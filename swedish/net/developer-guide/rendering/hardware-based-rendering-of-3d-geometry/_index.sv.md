---
title: Hårdvarubaserad hyllning av 3D Geometria
type: docs
weight: 30
url: /sv/net/hardware-based-rendering-of-3d-geometry/
description: Använder Aspose. 3D for .NET API, utvecklare kan programmera GPU (grafikbearbetningsenheten) och ställa in grafik hårdvara för att visa 3D geometri istället för den fasta funktionspipelinen
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, kan utvecklare programmera GPU (grafikbehandlingsenheten) och ställa in grafik hårdvara för att visa 3D geometri istället för den fasta funktionspipelinen I den här artikeln fokuserar vi på hårdvarabaserad rendering med [OpenGL 4. 0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). aspx) och [Vulkan Ordförande](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Skapa hårdvara och renter a 3D Geometria**
För att visa en 3D- geometri krävs en skuggar, buffertar och renderingstillstånd. Ingen av dem kan arbeta utan varandra.

- **Buffertar**- Triangellistor är enskilda trianglar som anges i ett matris som ibland kallas buffert. I en triangellista, varje triangel anges individuellt. Punkter i en triangel kan delas genom att använda index för att minska mängden data som måste skickas till grafik maskinvaran.
- **Skuggar**- Det definierar hur man omvandlar trianglar från världsutrymme till skärm och beräknar den slutliga pixelfärgen i GPU sidan
- **Render stater**- Det ger parametrar för GPU att rasterisera trianglarna i pixlar.

{{% alert color="primary" %}}

Vi har förberett ett demoprojekt. Se [Den här webbadressen för nedladdning](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

OpenGL-skuggande språk (GLSL) är det standardiserade språket på hög nivå för OpenGL-grafiken API. `InitRenderer`-metoden i `AssetBrowser/Controls/RenderView.cs`- filen under demoprogrammet (namn:AssetBrowser) visar enkel användning av GLSL med Aspose. 3D API. Det finns tre skugga typer som vanligen används: Vertex Shaders, Fragment Shaders och Geometri Shaders.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) klassen talar om för renderare, källkoden är för OpenGL- skuggningsspråk, den kan kompileras till [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) klass. [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable)-klassen definierar de variabler som används i skuggarn. Klassen `VariableSemantic` används för att identifiera skuggarvariablens semantiska, Aspose. 3D renderare förbereder automatiskt skuggarvariabelvärden beror på semantiken.
###  **Programmeringsprov för skuggar**
Det här kodexemplet initierar renderare och Shader för rutnätet. Du kan ladda ner komplett arbetsprojekt med detta exempel från [Här](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

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
###  **Programmeringsprov för buffert- och rendertillstånden**
Det här kodexemplet initierar bufferten och renderingstillståndet för rutnätet.

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
