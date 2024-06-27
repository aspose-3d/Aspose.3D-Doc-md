---
title: Offentlig API Ändrar i Aspose.3D 2.0.00
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Innehåll**

- [Adds Collada format](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Adds Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit interfaces and Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParameters classes](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Adds Aspose.ThreeD.Render.PostProcessing class](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Adds GetBoundingBox method to Aspose.ThreeD.Node class, Adds new classes Aspose.ThreeD.Utilities.BoundingBox and Aspose.ThreeD.Utilities.BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Real-time Rendering](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [AddData methods are added to Aspose.ThreeD.Entities.VertexElementUV class](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 1.7. 0 till 2.0.0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Lägger till formatet ColladaName**
I denna version (2.0.0), utvecklare kan importera Collada 3D filer, så egenskapen Collada läggs till i Aspose. 3D. Filformatklassen.
###  **Lägger till Aspose. 3D. Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit gränssnitt och Aspose. 3D. Render.Viewport/initialiseringException/Renderer/TextureType/DriverException/RenderFactory/RenderParameters klass**
De nya klasserna Viewport och Renderer är de viktigaste klasserna som hjälper till att fånga vyerna på en 3D-scen och spara till en text. eller fönster. Alla uppgifter om andra hjälpklasser är följande:

- **Aspose.ThreeD.Render.DriverException Class.**- Undantagen för den interna återgivaren är lindade som DriverException.
- **Aspose.ThreeD.Render.InitializationException-klass**- Detta undantag kastas utan att initialisera återgivningen, till exempel att initiera det på en dator som inte har något hårdvaruporter av OpenGL 4.0.
- **IRenderTarget-gränssnitt**- Det är basgränssnittet för IRenderTexture/IRenderWindow.
- **IRenderTexturgränssnitt**- Det gör det möjligt att återge scenen till en eller flera texturer (texturer finns i videominnet och kan överföras till systemminnet.
- **IRender- fönstergränssnitt**- Det gör det möjligt att göra scenen till fönster i realtid.
- **ITextureUnit**- ITextureUnit är texturprovtagaren i GPU-sidan och texturdata i CPU- eller GPU-minnet.
- **TextureType enume**- Det definierar typ av texturer, som Texture1D, Texture2D, Texture3D, CubeMap och Array2D.
- **RenderFactory Classy**- Det hjälper med att göra en scen till texturer eller fönster i realtid.
- **RenderParameters klass**- Det definierar parametrarna om hur man skapar renderingen mål som färg bitar, djup bitar, stencil bitar och dubbel buffert.

**Fånga vyer för en 3D Scene och teckning till en textur eller fönster**

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
###  **Lägger till Aspose.ThreeD.Render.PostProcessing klass**
PostProcessing klass tillåter utvecklare att använda realtidsfilter för bildbearbetning på den återgivna bilden. I denna version 2.0.0, har vi tillhandahållit 4 inbyggda efterbehandlingseffekter. Vi tillåter utvecklare att ha en egen egna efterbehandlingsalgoritm i den framtida versionen.

**Använd visuella effekter vid sparning av 3D Visningar**

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
###  **Lägger till GetBoundingBox- metoden till Aspose. 3D. Nodklass, Lägger till nya klasser Aspose. 3D. -Det är det. Boundingbox och Aspose. 3D. -Det är det. BoundingBoxExtentName**
Gränsrutan och BoundingBoxExtent- klasserna representerar avgränsande ruta i en 3D-nod. Utvecklare kan återställa kameran och beräkna höjden från avgränsande ruta. Den oändliga eller noll avgränsande lådan innebär att scenen inte har några geometrier och bara justera kamerans höjd när den är ändlig.
###  **Rendering i realtid**
Det gör det möjligt för utvecklare att utföra högpresterande realtids rendering på ett GUI ramverk som WinForms, det är ramverket oberoende, så de andra GUI-ramverken bör också stödja detta.
###  **AddData metoder läggs till i Aspose ThreeD.Entites.VertexElementUV klass**
VertexElementUV:s basklass har ändrats från VertexElementTemplate<Vector2>Till VertexElementTemplate<Vector4>, Det kommer bara att lagra Vector4 sedan 2.0.0, så två hjälpmedel metoder lades till för att användaren kunde lägga till en lista över Vector2 och Vector3 till VertexElementUV, det kommer att internt expandera Vector2/Vector3 till Vector4 och lämna restens fält noll:
