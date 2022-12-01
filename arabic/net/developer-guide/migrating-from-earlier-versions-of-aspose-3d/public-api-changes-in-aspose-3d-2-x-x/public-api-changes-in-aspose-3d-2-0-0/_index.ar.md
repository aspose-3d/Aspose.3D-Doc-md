---
title: Hangublic API hangمعلقة في Aspose.3D 2.0.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Contents Sأوماري**

- [Adds Collada تنسيق](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Adds Aspose.ThreeD](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Adds Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Adds GetBh9 ingBطريقة ox إلى Aspose.ThreeD.Node الفئة ، Adds فئات جديدة Aspose.ThreeD. tiliتيليتيز. Bh9 ingBox و Aspose.ThreeD. tiliتيليتيز.](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Dering ial-الوقت R](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [يتم إضافة طرق ddddData إلى Aspose.ThreeD.](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 1.7.0 إلى 2.0.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Adds Collada تنسيق**
In هذا الإصدار (2.0.0) ، يمكن للمطورين استيراد ملفات Collada 3D ، وبالتالي يتم إضافة خاصية Collada في Aspose.ThreeD. فئة ileFormat.
### **Adds Aspose.ThreeD**
Tهو جديد ieiewport و enenderer الطبقات الرئيسية التي تساعد على التقاط وجهات النظر من مشهد 3D وحفظ إلى نسيج أو نافذة. All تفاصيل الطبقات المساعدة الأخرى هي على النحو التالي:

- **Aspose.ThreeD**-يتم لف الاستثناءات من المستأجر الداخلي كما في وقت لاحق في وقت لاحق.
- **Aspose.ThreeD. ender اندر. InitializationEفئة xception**-يتم طرح هذا الاستثناء في حين فشل في تهيئة المستأجر ، على سبيل المثال لتهيئته على جهاز كمبيوتر لا يدعم الأجهزة OpenGL 4.0.
- **Ienواجهة واجهة**-It هو واجهة قاعدة من IenenderTexture/IenenderWindow.
- **Ienواجهة exture**-It يسمح لتقديم المشهد إلى واحد أو أكثر من القوام (القوام تقع في ذاكرة الفيديو ويمكن نقلها إلى ذاكرة النظام).
- **Ienواجهة indow**-It يسمح لتقديم المشهد إلى نافذة في الوقت الحقيقي.
- **Iexواجهة extureUنيت**-IexextureUnit هو عينة الملمس في الجانب GPside وبيانات الملمس في CPU أو GPU الذاكرة.
- **TextureTنوع enum**-It يحدد نوع من القوام ، مثل exexture1D ، Texture2D ، exexture3D ، CubeMap و Array2D.
- **الفئة الفنية**-It يساعد في تقديم مشهد للقوام أو نافذة في الوقت الحقيقي.
- **RenderPأقطار الفئة**-It يحدد المعلمات حول كيفية إنشاء الهدف تقديم مثل بت اللون ، بت عمق ، بت الاستنسل والتخزين المؤقت المزدوج.

**Apapture ieiewport من 3D cenسينا و ender ender إلى نسيج أو نافذة**

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
### **Adds Aspose.ThreeD.**
تسمح فئة roostProcessing للمطورين بتطبيق فلتر معالجة الصور في الوقت الحقيقي على الصورة المقدمة. In هذا الإصدار 2.0.0 ، لقد قدمنا 4 المدمج في آثار ما بعد المعالجة. سوف تسمح We للمطورين بالحصول على خوارزمية ما بعد المعالجة المخصصة الخاصة بهم في الإصدار المستقبلي.

**Apply ffisual ffffects على aving aving 3D ieiews**

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
### **Adds GetBh9 ingBطريقة ox إلى Aspose.ThreeD.Node الفئة ، Adds فئات جديدة Aspose.ThreeD. tiliتيليتيز. Bh9 ingBox و Aspose.ThreeD. tiliتيليتيز.**
The oundh9 ingBox و oundh9 ingBoxExالخيمة الطبقات تمثل صندوق الحدود من عقدة 3D. قد إعادة تعيين الكاميرا ، وحساب الارتفاع من صندوق الحدود. Tانه لانهائي أو لاغية صندوق الحدود يعني المشهد ليس لديه هندسية وضبط فقط ارتفاع الكاميرا عندما يكون محدود.
### **Dering ial-الوقت R**
It يسمح للمطورين لأداء تقديم عالية الأداء في الوقت الحقيقي على إطار GUI مثل orinForms ، انها GUindependent إطار مستقل ، وبالتالي فإن الأطر GGGالأخرى يجب أيضا دعم هذا.
### **يتم إضافة طرق ddddData إلى Aspose.ThreeD.**
لقد تغيرت فئة قاعدة he he erertexEleرقيق V من اللوحة الرئيسية<Vector2>إلى VertexE<Vector4>، فإنه سيتم تخزين فقط Vector4 منذ 2.0.0 ، لذلك تم إضافة طريقتين مساعد للسماح للمستخدم لإضافة قائمة من Vector2 و Vector3 إلى erertexEleentUV ، فإنه سيتم داخليا توسيع Vector2/Vector3 إلى Vector4 وترك بقية المجالات صفر:
