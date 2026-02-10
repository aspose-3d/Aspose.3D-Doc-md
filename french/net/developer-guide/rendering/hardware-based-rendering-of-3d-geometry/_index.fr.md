---
title: Rendu matériel basé sur la géométrie 3D
type: docs
weight: 30
url: /fr/net/hardware-based-rendering-of-3d-geometry/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent programmer le GPU (unité de traitement graphique) et configurer le matériel graphique pour rendre la géométrie 3D au lieu du pipeline de fonctions fixes.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, les développeurs peuvent programmer le GPU (unité de traitement graphique) et configurer le matériel graphique pour rendre la géométrie 3D au lieu du pipeline de fonctions fixes. Dans cet article, nous nous concentrons sur le rendu matériel en utilisant [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx et [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Créer du matériel et rendre une géométrie 3D**
Pour rendre une géométrie 3D, un shader, des tampons et un état de rendu sont requis. Aucun d'entre eux ne peut travailler l'un sans l'autre.

- **Tampons**-Les listes de triangles sont des triangles individuels spécifiés dans un tableau parfois appelé tampon. Dans une liste de triangle, chaque triangle est spécifié individuellement. Les points d'un triangle peuvent être partagés en utilisant des indices pour réduire la quantité de données qui doivent être transmises au matériel graphique.
- **Omandeurs**-Il définit comment transformer les triangles de l'espace du monde dans l'espace de l'écran et calculer la couleur finale du pixel dans le côté GPU
- **Rendre les États**-Il fournit des paramètres pour le GPU pour rastériser les triangles en pixels.

{{% alert color="primary" %}}

Nous avons préparé un projet démo. Veuillez vous référer à [Cette URL de téléchargement](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

OpenGL Shading Language (GLSL) est le langage d'ombrage standard de haut niveau pour les graphiques OpenGL API. La méthode `InitRenderer` dans le fichier `AssetBrowser/Controls/RenderView.cs` sous l'application démo (nom: AssetBrowser) démontre l'utilisation simple de GLSL en utilisant Aspose.3D API. Il existe trois types de shader couramment utilisés: Vertex Shaders, Fragment Shaders et Geometry Shaders.

La classe [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) indique au moteur de rendu, le code source est pour le langage d'ombrage OpenGL, il peut être compilé en [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) classe. La classe [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) définit les variables utilisées dans le shader. La classe `VariableSemantic` est utilisée pour identifier la sémantique de la variable shader, le rendu Aspose.3D préparera automatiquement les valeurs des variables shader en fonction de la sémantique.
###  **Échantillon de programmation pour Shader**
Cet exemple de code initialise le rendu et le shader pour la grille. Vous pouvez télécharger le projet de travail complet de cet exemple à partir de [Ici](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

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
###  **Échantillon de programmation pour l'état du tampon et du déposant**
Cet exemple de code initialise l'état de mémoire tampon et de rendu pour la grille.

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
