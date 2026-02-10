---
title: Donanım tabanlı 3D geometrisinin oluşturulması
type: docs
weight: 30
url: /tr/net/hardware-based-rendering-of-3d-geometry/
description: Using Aspose.3D for .NET API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. 
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. In this article, we focus on hardware-based rendering using [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Donanım oluşturun ve 3D geometrisini oluşturun**
3D geometrisini oluşturmak için gölgelendirici, tampon ve render durumu gereklidir. Hiçbiri birbirleri olmadan çalışamaz.

- **Buffers**-Triangle listeleri, bazen tampon olarak adlandırılan bir dizide belirtilen bireysel üçgenlerdir. In bir üçgen listesi, her üçgen ayrı ayrı belirtilir. Bir üçgenin kısıtlamaları, grafik donanımına geçmesi gereken veri miktarını azaltmak için endeksleri kullanarak paylaşılabilir.
- **Shaders**-It, üçgenleri dünya alanından ekran alanına nasıl dönüştüreceğini ve son piksel rengini GPside side olarak hesaplamayı tanımlar.
- **Render tates tates**-It, üçgenleri piksele dönüştürmek için GPU için parametreler sağlar.

{{% alert color="primary" %}}

We have prepared a demo project. Please refer to [this download URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

The OpenGL Shading Language (GLSL) is the standard high level shading language for the OpenGL graphics API. The `InitRenderer` method in `AssetBrowser/Controls/RenderView.cs` file under the demo application (name:AssetBrowser) demonstrates the simple use of GLSL using Aspose.3D API. There are three shader types commonly used: Vertex Shaders, Fragment Shaders and Geometry Shaders.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) sınıfı kiracıya söyler, kaynak kodu opengl gölgeleme dili içindir, [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) sınıfına derlenebilir. [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) sınıfı gölgelendiricide kullanılan değişkenleri tanımlar. `VariableSemantic` sınıfı, gölgelendirici değişkeninin semantik, Aspose.3D renderer otomatik olarak gölgelendirici değişken değerlerini semantiklere göre hazırlayacaktır.
###  **Srogramming SShader için yeterli**
Bu kod örneği, ızgara için renderer ve gölgelendirici başlatır. Bu örneğin tam çalışma projesini [Burada](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering) 'dan indirebilirsiniz.

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
###  **Brogramming ffer Buffer ve Render State için yeterli**
Tkod örneği tamponu başlatır ve ızgara için durum oluşturur.

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
