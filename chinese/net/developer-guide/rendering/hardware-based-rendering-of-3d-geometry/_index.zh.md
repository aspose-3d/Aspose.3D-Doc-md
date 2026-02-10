---
title: 3D 几何图形的基于硬件的呈现
type: docs
weight: 30
url: /zh/net/hardware-based-rendering-of-3d-geometry/
description: 使用 Aspose.3D for .NET API，开发人员可以对GPU (图形处理单元) 进行编程，并设置图形硬件来渲染 3D 几何图形，而不是固定函数管道。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API，开发人员可以对GPU (图形处理单元) 进行编程，并设置图形硬件来渲染 3D 几何图形，而不是固定函数管道。在本文中，我们重点介绍使用 [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml) 、 [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx) 、 [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) 和 [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo) 的基于硬件的渲染。

{{% /alert %}}
##  **创建硬件并渲染 3D 几何体**
若要渲染 3D 几何体，需要着色器、缓冲区和渲染状态。他们都离不开彼此。

- **缓冲区**-三角形列表是在数组中指定的单个三角形，有时被称为缓冲区。在三角形列表中，每个三角形都是单独指定的。可以通过使用索引来减少必须传递给图形硬件的数据量来共享三角形的点。
- **着色器**-它定义了如何将三角形从世界空间转换为屏幕空间并计算GPU侧的最终像素颜色
- **渲染状态**-它为GPU提供了参数，以将三角形光栅化为像素。

{{% alert color="primary" %}}

我们准备了一个演示项目。请参阅 [这个下载网址](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering)。

{{% /alert %}}

OpenGL着色语言 (GLSL) 是OpenGL图形 API 的标准高级着色语言。演示应用程序 (名称: AssetBrowser) 下的 `AssetBrowser/Controls/RenderView.cs` 文件中的 `InitRenderer` 方法演示了使用 Aspose.3D API 的GLSL的简单用法。有三种常用的着色器类型: 顶点着色器，片段着色器和几何着色器。

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) 类告诉渲染器，源代码是为OpenGL着色语言编写的，可以编译成 [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) 类。[`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) 类定义着色器中使用的变量。`VariableSemantic` 类用于标识着色器变量的语义 Aspose。3D 渲染器将根据语义自动准备着色器变量值。
###  **着色器的编程示例**
此代码示例初始化网格的渲染器和着色器。您可以从 [这里](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering) 下载此示例的完整工作项目。

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
###  **缓冲区和渲染状态的编程示例**
此代码示例初始化网格的缓冲区和渲染状态。

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
