---
title: Öffentliche API Änderungen in Aspose.3D 2.0.0
type: docs
weight: 20
url: /de/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Inhalts übersicht**

- [Fügt das Format Collada hinzu](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Fügt Aspose.ThreeD.Render.IRender Target/IRender Texture/Irender Window/ITexture Unit-Schnitts tellen und Aspose.ThreeD.Render.Viewport/Initial isierung Exception/Renderer/Texture Type/Driver Exception/Render Factory/RenderParameters-Klassen hinzu](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Fügt Aspose.ThreeD.Render.PostProcessing-Klasse hinzu](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Fügt der GetBoundingBox-Methode zu Aspose.ThreeD hinzu. Knoten klasse, Fügt neue Klassen Aspose.ThreeD hinzu. Utilities.BoundingBox und Aspose.ThreeD. Dienst programme. Bounding Box Extent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Echtzeit-Rendering](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [AddData-Methoden werden zu Aspose.ThreeD. Entitäten. VertexElementUV-Klasse hinzugefügt](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 1.7.0 bis 2.0.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Fügt das Format Collada hinzu**
In dieser Version (2.0.0) können Entwickler Collada 3D-Dateien importieren, sodass die Eigenschaft Collada in der Klasse Aspose.ThreeD hinzugefügt wird.
### **Fügt Aspose.ThreeD.Render.IRender Target/IRender Texture/Irender Window/ITexture Unit-Schnitts tellen und Aspose.ThreeD.Render.Viewport/Initial isierung Exception/Renderer/Texture Type/Driver Exception/Render Factory/RenderParameters-Klassen hinzu**
Die neuen Viewport-und Renderer-Klassen sind die Hauptklassen, mit denen die Ansichten einer 3D-Szene erfasst und in einer Textur oder einem Fenster gespeichert werden können. Alle Details anderer helfender Klassen sind wie folgt:

- **Aspose.ThreeD.Render.Driver Ausnahme klasse**-Die Ausnahmen des internen Renderers werden als Driver Exception eingewickelt.
- **Aspose.ThreeD.Render.Initial isierung Ausnahme klasse**-Diese Ausnahme wird ausgelöst, während der Renderer nicht initial isiert werden kann, z. B. um ihn auf einem Computer zu initial isieren, der keine Hardware-Unterstützung von OpenGL 4.0 hat.
- **IrenderTarget-Schnitts telle**-Es ist die Basis-Schnitts telle von IRender Texture/Ireder Window.
- **IrenderTexture-Schnitts telle**-Es ermöglicht das Rendern der Szene auf eine oder mehrere Texturen (Texturen befinden sich im Videosp eicher und können in den Systemsp eicher übertragen werden).
- **IrenderWindow-Schnitts telle**-Es erlaubt, die Szene in Echtzeit zum Fenster zu rendern.
- **IITextureUnit-Schnitts telle**-Itexture Unit ist der Textur-Sampler auf der GPU-Seite und die Textur daten im CPU-oder GPU-Speicher.
- **Texture Type enum**-Es definiert die Art der Texturen, wie Texture1D, Texture2D, Texture3D, CubeMap und Array2D.
- **Render Factory Klasse**-Es hilft beim Rendern einer Szene zu Texturen oder Fenster in Echtzeit.
- **RenderParameter-Klasse**-Es definiert die Parameter zum Erstellen des Render ziels wie Farbbits, Tiefen bits, Schablonen bits und Doppel pufferung.

**Erfassen Sie die View ports einer 3D-Szene und Render zu einer Textur oder einem Fenster**

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
### **Fügt Aspose.ThreeD.Render.PostProcessing-Klasse hinzu**
Mit der PostProcessing-Klasse können Entwickler Echtzeit-Bild verarbeitung filter auf das gerenderte Bild anwenden. In dieser Version 2.0.0 haben wir 4 integrierte Nach bearbeitungs effekte bereit gestellt. Wir werden Entwicklern erlauben, ihren eigenen benutzer definierten Post-Processing-Algorithmus in der zukünftigen Version zu haben.

**Visuelle Effekte beim Speichern von 3D-Ansichten anwenden**

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
### **Fügt der GetBoundingBox-Methode zu Aspose.ThreeD hinzu. Knoten klasse, Fügt neue Klassen Aspose.ThreeD hinzu. Utilities.BoundingBox und Aspose.ThreeD. Dienst programme. Bounding Box Extent**
Die Klassen Bounding Box und Bounding Box Extent repräsentieren die Begrenzung sbox eines Knotens 3D. Entwickler können die Kamera zurücksetzen und die Höhe aus dem Begrenzung sfeld berechnen. Die unendliche oder Null-Begrenzung sbox bedeutet, dass die Szene keine Geometrien hat und die Höhe der Kamera nur anpasst, wenn sie endlich ist.
### **Echtzeit-Rendering**
Es ermöglicht Entwicklern, leistungs starkes Echtzeit-Rendering auf einem GUI-Framework wie Win Forms durch zuführen. Es ist GUI-Framework-unabhängig, sodass die anderen GUI-Frameworks dies ebenfalls unterstützen sollten.
### **AddData-Methoden werden zu Aspose.ThreeD. Entitäten. VertexElementUV-Klasse hinzugefügt**
Die Basis klasse des Vertex ElementUV hat sich von Vertex Element Template geändert<Vector2>Zu Vertex Element Template<Vector4>Es wird nur Vector4 seit 2.0.0 gespeichert. Daher wurden zwei Hilfs methoden hinzugefügt, mit denen der Benutzer eine Liste von Vector2 und Vector3 zu Vertex ElementUV hinzufügen kann. Es erweitert den Vector2/Vector3 intern zu Vector4 und lässt die restlichen Felder Null:
