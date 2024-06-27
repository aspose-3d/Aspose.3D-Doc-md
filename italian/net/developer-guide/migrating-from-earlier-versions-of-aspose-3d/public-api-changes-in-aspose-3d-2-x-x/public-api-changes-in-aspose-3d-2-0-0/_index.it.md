---
title: Variazioni pubbliche di API in Aspose.3D 2.0.0
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Contenuto sommario**

- [Aggiunge il formato Collada](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Aggiunge Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit interfacce e Aspose.ThreeD.Render.Viewport/InitializationException/RenderParameters classi](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Aggiunge Aspose.ThreeD.Render.PostProcessing Class](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Aggiunge il metodo GetBoundingBox a Aspose. Classe ThreeD.Node, aggiunge nuove classi Aspose.ThreeD.Utilities.BoundingBox e Aspose.ThreeD.Utilities. BoundBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Rendering in tempo reale](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [I metodi AddData vengono aggiunti alla classe Aspose.ThreeD.Entities.VertexElementUV](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche a Aspose.3D API dalla versione da 1.7.0 a 2.0.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **Aggiunge il formato Collada**
In questa versione (2.0.0), gli sviluppatori possono importare file Collada 3D, quindi la proprietà Collada viene aggiunta nella classe Aspose.ThreeD.FileFormat.
###  **Aggiunge Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit interfacce e Aspose.ThreeD.Render.Viewport/InitializationException/RenderParameters classi**
Le nuove classi Viewport e Renderer sono le classi principali che aiutano a catturare le visualizzazioni di una scena 3D e salvarle in una texture o in una finestra. Tutti i dettagli di altre classi di aiuto sono i seguenti:

- **Aspose.ThreeD.Render.DriverException class**-Le eccezioni del renderer interno sono racchiuse come DriverException.
- **Aspose. Classe ThreeD.Render.InitializationException**-Questa eccezione viene generata mentre non si riesce a inizializzare il renderer, ad esempio per inizializzarlo su un computer che non ha il supporto hardware di OpenGL 4.0.
- **Interfaccia IRenderTarget**-È l'interfaccia di base di IRenderTexture/IRenderWindow.
- **Interfaccia IRenderTexture**-Permette di rendere la scena a una o più trame (le trame si trovano nella memoria video e possono essere trasferite nella memoria di sistema).
- **Interfaccia IRenderWindow**-Permette di rendere la scena alla finestra in tempo reale.
- **Interfaccia ITextureUnit**-ITextureUnit è il campionatore di texture sul lato GPU e i dati di texture nella memoria CPU o GPU.
- **TextureType enum**-Definisce il tipo di trame, come Texture1D, Texture2D, Texture3D, CubeMap e Array2D.
- **Classe RenderFactory**-Aiuta a rendere una scena su trame o finestre in tempo reale.
- **Classe RenderParametri**-Definisce i parametri su come creare il target di rendering come bit di colore, bit di profondità, bit di stencil e doppio buffering.

**Cattura le visualizzazioni di una scena 3D e rendita a una texture o finestra**

**C#**

{{< highlight "csharp" >}}

 // load an existing 3D scene

Scene scene = new Scene("scene.obj");

// create an instance of the camera

Camera camera = new Camera();

scene.RootNode.CreateChildNode("camera", camera).Transform.Translation = new Vector3(2, 44, 66);

// set the target

camera.LookAt = new Vector3(50, 12, 0);

//create a light

scene.RootNode.CreateChildNode("light", new Light() {Color = new Vector3(Color.White), LightType =  LightType.Point}).Transform.Translation = new Vector3(26, 57, 43);

// the CreateRenderer will create a hardware OpenGL-backend renderer

// and some internal initializations will be done.

// when the renderer left using the scope, the unmanaged hardware resources will also be disposed

using (var renderer = Renderer.CreateRenderer())

{

    renderer.EnableShadows = false;

    // create a new render target that renders the scene to texture(s)

    // use default render parameters

    // and one output targets

    // size is 1024 x 1024

    // this render target can have multiple render output textures, but here we only need one output.

    // The other textures and depth textures are mainly used by deferred shading in the future.

    // but you can also access the depth texture through IRenderTexture.DepthTeture

    // use CreateRenderWindow method to render in window, like:

    // window = renderer.RenderFactory.CreateRenderWindow(new RenderParameters(), Handle);

    using (IRenderTexture rt = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(), 1, 1024, 1024))

    {

        //this render target has one viewport to render, the viewport occupies the 100% width and 100% height

        Viewport vp = rt.CreateViewport(camera, new RelativeRectangle() {ScaleWidth = 1, ScaleHeight = 1});

        //render the target and save the target texture to external file

        renderer.Render(rt);

        rt.Targets[0].Save("file-1viewports.png", ImageFormat.Png);

        //now let's change the previous viewport only uses the half left side(50% width and 100% height)

        vp.Area = new RelativeRectangle() {ScaleWidth = 0.5f, ScaleHeight = 1};

        //and create a new viewport that occupies the 50% width and 100% height and starts from 50%

        //both of them are using the same camera, so the rendered content should be the same

        rt.CreateViewport(camera, new RelativeRectangle() {ScaleX = 0.5f, ScaleWidth = 0.5f, ScaleHeight = 1});

        //but this time let's increase the field of view of the camera to 90 degree so it can see more part of the scene

        camera.FieldOfView = 90;

        renderer.Render(rt);

        rt.Targets[0].Save("file-2viewports.png", ImageFormat.Png);

    }

}

{{< /highlight >}}
###  **Aggiunge Aspose.ThreeD.Render.PostProcessing Class**
La classe PostProcessing consente agli sviluppatori di applicare il filtro di elaborazione delle immagini in tempo reale all'immagine renderizzata. In questa versione 2.0.0, abbiamo fornito 4 effetti di post-elaborazione integrati. Consentiremo agli sviluppatori di avere il proprio algoritmo di post-elaborazione personalizzato nella versione futura.

**Applica effetti visivi per risparmiare 3D visualizzazioni**

**C#**

{{< highlight "csharp" >}}

 // load an existing 3D scene

Scene scene = new Scene("scene.obj");

// create an instance of the camera

Camera camera = new Camera();

scene.RootNode.CreateChildNode("camera", camera).Transform.Translation = new Vector3(2, 44, 66);

// set the target

camera.LookAt = new Vector3(50, 12, 0);

//create a light

scene.RootNode.CreateChildNode("light", new Light() { Color = new Vector3(Color.White), LightType = LightType.Point }).Transform.Translation = new Vector3(26, 57, 43);

// the CreateRenderer will create a hardware OpenGL-backend renderer, more renderer will be added in the future

// and some internal initializations will be done.

// when the renderer left using the scope, the unmanaged hardware resources will also be disposed

using (var renderer = Renderer.CreateRenderer())

{

    renderer.EnableShadows = false;

    // create a new render target that renders the scene to texture(s)

    // use default render parameters

    // and one output targets

    // size is 1024 x 1024

    // this render target can have multiple render output textures, but here we only need one output.

    // The other textures and depth textures are mainly used by deferred shading in the future.

    // but you can also access the depth texture through IRenderTexture.DepthTeture

    using (IRenderTexture rt = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(), 1, 1024, 1024))

    {

        // this render target has one viewport to render, the viewport occupies the 100% width and 100% height

        Viewport vp = rt.CreateViewport(camera, new RelativeRectangle() { ScaleWidth = 1, ScaleHeight = 1 });

        //render the target and save the target texture to external file

        renderer.Render(rt);

        rt.Targets[0].Save("Original_viewport.png", ImageFormat.Png);

        // create a post-processing effect

        PostProcessing pixelation = renderer.GetPostProcessing("pixelation");

        renderer.PostProcessings.Add(pixelation);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_pixelation.png", ImageFormat.Png);

        //clear previous post-processing effects and try another one

        PostProcessing grayscale = renderer.GetPostProcessing("grayscale");

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(grayscale);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_grayscale.png", ImageFormat.Png);

        //we can also combine post-processing effects

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(grayscale);

        renderer.PostProcessings.Add(pixelation);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_grayscale+pixelation.png", ImageFormat.Png);

        //clear previous post-processing effects and try another one

        PostProcessing edgedetection = renderer.GetPostProcessing("edge-detection");

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(edgedetection);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_edgedetection.png", ImageFormat.Png);

        //clear previous post-processing effects and try another one

        PostProcessing blur = renderer.GetPostProcessing("blur");

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(blur);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_blur.png", ImageFormat.Png);

    }

}

{{< /highlight >}}
###  **Aggiunge il metodo GetBoundingBox a Aspose. Classe ThreeD.Node, aggiunge nuove classi Aspose.ThreeD.Utilities.BoundingBox e Aspose.ThreeD.Utilities. BoundBoxExtent**
Le classi BoundingBox e BoundingBoxExtent rappresentano il riquadro di delimitazione di un nodo 3D. Gli sviluppatori possono reimpostare la fotocamera e calcolare l'elevazione dal riquadro di delimitazione. Il riquadro di delimitazione infinito o nullo significa che la scena non ha geometrie e regola l'elevazione della telecamera solo quando è finita.
###  **Rendering in tempo reale**
Consente agli sviluppatori di eseguire il rendering in tempo reale ad alte prestazioni su un framework GUI come WinForms, è indipendente dal framework GUI, quindi anche gli altri framework GUI dovrebbero supportarlo.
###  **I metodi AddData vengono aggiunti alla classe Aspose.ThreeD.Entities.VertexElementUV**
La classe base di VertexElementUV è cambiata da VertexElementTemplate<Vector2>A VertexElementTemplate<Vector4>, Memorizzerà Vector4 solo da 2.0.0, quindi sono stati aggiunti due metodi di supporto per consentire all'utente di aggiungere un elenco di Vector2 e Vector3 a VertexElementUV, espanderà internamente Vector2/Vector3 a Vector4 e lascerà zero i campi rimanenti:
