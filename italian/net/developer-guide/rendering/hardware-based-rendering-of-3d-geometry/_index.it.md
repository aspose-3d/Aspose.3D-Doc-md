---
title: Rendering basato su hardware di 3D geometria
type: docs
weight: 30
url: /it/net/hardware-based-rendering-of-3d-geometry/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono programmare la GPU (unità di elaborazione grafica) e configurare l'hardware grafico per il rendering della geometria 3D invece della pipeline di funzioni fisse.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, gli sviluppatori possono programmare la GPU (unità di elaborazione grafica) e configurare l'hardware grafico per il rendering della geometria 3D invece della pipeline di funzioni fisse. In questo articolo, ci concentriamo sul rendering basato su hardware utilizzando [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirettX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirettX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) e [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Crea hardware e renderizza una geometria di 3D**
Per rendere una geometria 3D, sono necessari uno shader, buffer e stato di rendering. Nessuno di loro può lavorare l'uno senza l'altro.

- **Tamponi**-Gli elenchi dei triangoli sono triangoli individuali specificati in un array a volte indicato come buffer. In un elenco di triangolo, ogni triangolo viene specificato individualmente. I punti di un triangolo possono essere condivisi utilizzando gli indici per ridurre la quantità di dati che devono essere passati all'hardware grafico.
- **Ombanti**-Definisce come trasformare i triangoli dallo spazio mondiale nello spazio dello schermo e calcolare il colore del pixel finale sul lato GPU
- **Stati di rendita**-Fornisce parametri per la GPU per rasterizzare i triangoli in pixel.

{{% alert color="primary" %}}

Abbiamo preparato un progetto demo. Fai riferimento a [Questo URL di download](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

OpenGL Shading Language (GLSL) è il linguaggio di ombreggiatura standard di alto livello per la grafica OpenGL API. Il metodo `InitRenderer` nel file `AssetBrowser/Controls/RenderView.cs` sotto l'applicazione demo (nome: AssetBrowser) mostra il semplice utilizzo di GLSL utilizzando Aspose.3D API. Esistono tre tipi di shader comunemente usati: Vertex Shader, Frammento Shader e Geometry Shaders.

La classe [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) dice al renderer, il codice sorgente è per il linguaggio di ombreggiatura OpenGL, può essere compilato in [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) classe. La classe [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) definisce le variabili utilizzate nello shader. La classe `VariableSemantic` viene utilizzata per identificare la semantica della variabile shader, Aspose. Il renderer 3D preparerà automaticamente i valori delle variabili shader a seconda della semantica.
###  **Campione di programmazione per Shader**
Questo esempio di codice inizializza renderer e Shader per la griglia. Puoi scaricare il progetto di lavoro completo di questo esempio da [Qui](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

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
###  **Campione di programmazione per il buffer e lo stato di rendering**
Questo esempio di codice inizializza il buffer e lo stato di rendering per la griglia.

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
