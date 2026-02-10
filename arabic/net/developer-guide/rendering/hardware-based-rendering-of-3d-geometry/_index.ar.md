---
title: تقديم قائم على الأجهزة بقيمة 3D هندسة
type: docs
weight: 30
url: /ar/net/hardware-based-rendering-of-3d-geometry/
description: باستخدام Aspose.3D for .NET API ، يمكن للمطورين برمجة وحدة معالجة الرسومات (وحدة معالجة الرسومات) وإعداد أجهزة الرسومات لتقديم هندسة 3D بدلاً من خط أنابيب الوظائف الثابتة.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. In this article, we focus on hardware-based rendering using [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **إنشاء الأجهزة وتقديم هندسة 3D**
مطلوب تقديم شكل هندسي 3D ، تظليل ، مخازن وحالة تقديم. لا يمكن لأي منهم العمل دون الآخر.

- **Uuffers**-قوائم riangle Tهي مثلثات فردية محددة في صفيف يشار إليها أحيانا باسم المخزن المؤقت. In قائمة مثلث ، يتم تحديد كل مثلث بشكل فردي. يمكن مشاركة oinللمثلث باستخدام مؤشرات لتقليل كمية البيانات التي يجب تمريرها إلى أجهزة الرسومات.
- **Sهادرز**-It يحدد كيفية تحويل المثلثات من الفضاء العالمي إلى مساحة الشاشة وحساب لون بكسل النهائي في الجانب GPU
- **Render تيتس**-يوفر It المعلمات ل GPraraالمثلثات إلى بكسل.

{{% alert color="primary" %}}

قمنا بإعداد مشروع تجريبي. يرجى الرجوع إلى [هذا تحميل URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

لغة تظليل OpenGL (GLSL) هي لغة تظليل قياسية عالية المستوى لرسومات OpenGL API. توضح طريقة `InitRenderer` في ملف `AssetBrowser/Controls/RenderView.cs` ضمن التطبيق التجريبي (الاسم: AssetBrowser) الاستخدام البسيط لـ GLSL باستخدام Aspose.3D API. هناك ثلاثة أنواع من التظليل شائعة الاستخدام: تظليل الرأس ، تظليل الشظية ، تظليل الهندسة.

فئة [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) تخبر المستعرض ، رمز المصدر هو لغة تظليل OpenGL ، ويمكن تجميعها إلى فئة [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). تحدد فئة [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) المتغيرات المستخدمة في التظليل. تُستخدم فئة `VariableSemantic` لتحديد الدلالية لمتغير التظليل ، Aspose. سيقوم المستعرض 3D بإعداد قيم متغير التظليل تلقائيًا بناءً على الدلالات.
###  **Pروغرامينغ ple وافرة ل Shader**
هذا المثال رمز تهيئة العارضين وتظليل للشبكة. يمكنك تنزيل مشروع العمل الكامل لهذا المثال من [هنا](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
private void InitRenderer()
{
    // Create a default camera, because it's required during the viewport's creation.
    camera = new Camera();
    Scene.RootNode.CreateChildNode("camera", camera);
    // Create the renderer and render window from window's native handle
    renderer = Renderer.CreateRenderer();
    // Right now we only support native window handle from Microsoft Windows
    // We'll support more platform on user's demand.
    window = renderer.RenderFactory.CreateRenderWindow(new RenderParameters(), Handle);
    // Create 4 viewports, the viewport's area is meanless here because we'll change it to the right area in the SetViewports later
    viewports = new[]
    {
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1)),
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1)),
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1)),
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1))
    };
    SetViewports(1);


    //initialize shader for grid

    GLSLSource src = new GLSLSource();
    src.VertexShader = @"#version 330 core
    layout (location = 0) in vec3 position;
    uniform mat4 matWorldViewProj;
    void main()
    {
        gl_Position = matWorldViewProj * vec4(position, 1.0f);
    }";
                src.FragmentShader = @"#version 330 core
    out vec4 color;
    void main()
    {
        color = vec4(1, 1, 1, 1);
    }";
    // Define the input format used by GLSL vertex shader the format is struct ControlPoint { FVector3 Position;}
    VertexDeclaration fd = new VertexDeclaration();
    fd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);
    // Compile shader from GLSL source code and specify the vertex input format
    gridShader = renderer.RenderFactory.CreateShaderProgram(src, fd);
    // Connect GLSL uniform to renderer's internal variable
    gridShader.Variables = new ShaderVariable[]
    {
        new ShaderVariable("matWorldViewProj", VariableSemantic.MatrixWorldViewProj)
    };

    SceneUpdated("");
}

{{< /highlight >}}
###  **Pروغرامينغ ple وافرة ل Bأوفر و Render تايت**
Tله رمز المثال يبدأ المخزن المؤقت وتقديم الدولة للشبكة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
class Grid : ManualEntity
{
    public Grid(Renderer renderer, ShaderProgram shader)
    {
        // Render state for grid
        RenderState = renderer.RenderFactory.CreateRenderState();
        RenderState.DepthTest = true;
        RenderState.DepthMask = true;
        this.Shader = shader;
        // Define the format of the control point to render the line
        VertexDeclaration vd = new VertexDeclaration();
        vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);
        // and create a vertex buffer for storing this kind of data
        this.VertexBuffer = renderer.RenderFactory.CreateVertexBuffer(vd);
        // Draw the primitive as lines
        this.DrawOperation = DrawOperation.Lines;
        this.RenderGroup = RenderQueueGroupId.Geometries;

        List<FVector3> lines = new List<FVector3>();
        for (int i = -10; i <= 10; i++)
        {
            // Draw - line
            lines.Add(new FVector3(i, 0, -10));
            lines.Add(new FVector3(i,0, 10));


            // Draw | line
            lines.Add(new FVector3(-10, 0, i));
            lines.Add(new FVector3(10, 0, i));
        }
        // Put it to vertex buffer
        VertexBuffer.LoadData(lines.ToArray());
    }
}

{{< /highlight >}}
