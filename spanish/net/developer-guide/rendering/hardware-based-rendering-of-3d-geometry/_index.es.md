---
title: Renderización basada en hardware de geometría 3D
type: docs
weight: 30
url: /es/net/hardware-based-rendering-of-3d-geometry/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden programar la GPU (unidad de procesamiento de gráficos) y configurar el hardware de gráficos para renderizar la geometría 3D en lugar de la canalización de funciones fijas.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, los desarrolladores pueden programar la GPU (unidad de procesamiento de gráficos) y configurar el hardware de gráficos para renderizar la geometría 3D en lugar de la canalización de función fija. En este artículo, nos centramos en la representación basada en hardware utilizando [OpenGL 4,0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx y [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Crear hardware y render una geometría 3D**
Para renderizar una geometría 3D, se requiere un shader, buffers y un estado de render. Ninguno de ellos puede trabajar el uno sin el otro.

- **Tampones**-Las listas de triángulos son triángulos individuales especificados en una matriz que a veces se denomina búfer. En una lista de triángulos, cada triángulo se especifica individualmente. Los puntos de un triángulo se pueden compartir mediante índices para reducir la cantidad de datos que se deben pasar al hardware gráfico.
- **Shaders**-Define cómo transformar los triángulos del espacio del mundo en el espacio de la pantalla y calcular el color del píxel final en el lado de la GPU
- **Estados de render**-Proporciona parámetros para que la GPU rasterice los triángulos en píxeles.

{{% alert color="primary" %}}

Hemos preparado un proyecto de demostración. Por favor refiérase a [Esta URL de descarga](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

El Lenguaje de Sombreado OpenGL (GLSL) es el lenguaje estándar de sombreado de alto nivel para los gráficos OpenGL API. El método `InitRenderer` en el archivo `AssetBrowser/Controls/RenderView.cs` bajo la aplicación de demostración (nombre: AssetBrowser) demuestra el uso simple de GLSL usando Aspose.3D API. Hay tres tipos de sombreadores comúnmente utilizados: Vertex Shaders, Fragment Shaders y Geometry Shaders.

La clase [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) le dice al renderizador, el código fuente es para el lenguaje de sombreado OpenGL, se puede compilar a la clase [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). La clase [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) define las variables utilizadas en el shader. La clase `VariableSemantic` se usa para identificar la semántica de la variable de sombreado, Aspose.3D El renderizador preparará automáticamente los valores de la variable de sombreado según la semántica.
###  **Muestra de programación para Shader**
Este ejemplo de código inicializa el renderizador y el sombreador para la cuadrícula. Puede descargar el proyecto de trabajo completo de este ejemplo desde [Aquí](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

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
###  **Muestra de programación para el búfer y el estado de renderización**
Este ejemplo de código inicializa el búfer y el estado de procesamiento para la cuadrícula.

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
