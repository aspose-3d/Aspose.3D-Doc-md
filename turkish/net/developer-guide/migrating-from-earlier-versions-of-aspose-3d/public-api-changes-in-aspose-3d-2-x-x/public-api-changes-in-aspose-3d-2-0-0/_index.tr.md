---
title: Kamu API Aspose içinde değişir. 3D 2.0.0
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Contents Summary**

- [Collada formatı ekler](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Aspose ekler. threed. render. irendertarget/irenderwindow/irenderwindow/itextureunit arabirimleri ve Aspose. threed. view. viewport/initializationexception/renderer/texturetype/driverexception/renderfactory/renderparameters sınıfları](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Adds Aspose.ThreeD.Render.PostProcessing class](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Adds GetBoundingBox method to Aspose.ThreeD.Node class, Adds new classes Aspose.ThreeD.Utilities.BoundingBox and Aspose.ThreeD.Utilities.BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Real-zaman dering endering](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [AddData methods are added to Aspose.ThreeD.Entities.VertexElementUV class](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

Bu belge, Aspose.3D API sürüm 1.7.0 'dan 2.0.0 'e kadar olan değişiklikleri açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. Sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'daki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
###  **Collada formatı ekler**
In this version (2.0.0), developers can import Collada 3D files, so the Collada property is added in Aspose.ThreeD.FileFormat class.
###  **Aspose ekler. threed. render. irendertarget/irenderwindow/irenderwindow/itextureunit arabirimleri ve Aspose. threed. view. viewport/initializationexception/renderer/texturetype/driverexception/renderfactory/renderparameters sınıfları**
Yeni bakış açısı ve renderer sınıfları, 3D sahnesinin görüşlerini yakalamanıza ve bir doku veya pencereye kaydetmenize yardımcı olan ana sınıflardır. Diğer yardım sınıflarının tüm detayları aşağıdaki gibidir:

- **Aspose. threed. render. driverexception sınıfı**-İç kiracının istisnaları Driverriverxception olarak sarılır.
- **Aspose. threed. render. initializationexception sınıfı**-Bu istisna, kiracıyı başlatamazken atılır, örneğin Openpen4.0 4.0 donanım desteği olmayan bir bilgisayarda başlatır.
- **IRenderararget arayüzü**-It, Ienender. exture/Ienender. indow'un temel arayüzüdür.
- **IRenderexexture arayüzü**-It, sahneyi bir veya daha fazla dokuya dönüştürmeye izin verir (dokular video belleğinde bulunur ve sistem belleğine aktarılabilir).
- **IRenderinindow arayüzü**-It, sahneyi gerçek zamanlı olarak pencereye dönüştürmeye izin verir.
- **ITexturenit nit arayüzü**-ITexturenit nit, Gside side side ve Cmemory memory veya Gmemory memory bellekteki doku verilerinde doku örnekleyicidir.
- **Textureyype enum**-It, Texture1D, Texture2D, Texture3D, uubeap ap ve Array2. gibi dokuların türünü tanımlar.
- **Rendertory actory sınıfı**-It, bir sahneyi dokulara veya pencereye gerçek zamanlı olarak oluşturmaya yardımcı olur.
- **Renderenarameters sınıfı**-It, renk bitleri, derinlik bitleri, şablon bitleri ve çift tamponlama gibi render hedefinin nasıl oluşturulacağı ile ilgili parametreleri tanımlar.

**3D sahnesinin görüntülerini yakalayın ve bir doku veya pencereye dönüştürün**

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
###  **Adds Aspose.ThreeD.Render.PostProcessing class**
Post. rocessing sınıfı, geliştiricilerin gerçek zamanlı görüntü işleme filtresini işlenmiş görüntüye uygulamasına izin verir. In bu sürüm 2.0.0, 4 dahili işlem sonrası efekt sağladık. We, geliştiricilerin gelecekteki sürümde kendi özel işlem sonrası algoritmalarına sahip olmasına izin verecektir.

**3D görünümlerini kaydetme üzerine görsel efektler uygulayın**

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
###  **Adds GetBoundingBox method to Aspose.ThreeD.Node class, Adds new classes Aspose.ThreeD.Utilities.BoundingBox and Aspose.ThreeD.Utilities.BoundingBoxExtent**
Boundingbox ve boundingbox. sınıfları, 3D düğümünün sınırlama kutusunu temsil eder. Geliştiriciler kamerayı sıfırlayabilir ve sınırlama kutusundan yüksekliği hesaplayabilir. Sonsuz veya boş sınırlama kutusu, sahnenin geometrisi olmadığı ve sonlu olduğunda sadece kameranın yüksekliğini ayarladığı anlamına gelir.
###  **Real-zaman dering endering**
It, geliştiricilerin Wininorms gibi bir Ginçerçeve üzerinde yüksek performanslı gerçek zamanlı işleme gerçekleştirmelerine izin verir, Gframework çerçeve-bağımsız, bu yüzden diğer frameframeframeçerçeveler de bunu desteklemelidir.
###  **AddData methods are added to Aspose.ThreeD.Entities.VertexElementUV class**
The VertexElementUV 'in temel sınıfı VertexElementTemplate 'den değişti<Vector2>VertexElementTemplate için<Vector4>2.ector4'ü 2.0.0 'dan beri saklayacak, bu yüzden kullanıcının Vector2 ve Vector3'ün bir listesini erertexElementUV 'e eklemesine izin vermek için iki yardımcı yöntem eklendi, dahili olarak Vector2/Vector3'ü Vector4'e genişletecek ve dinlenme alanlarını sıfır bırakacak:
