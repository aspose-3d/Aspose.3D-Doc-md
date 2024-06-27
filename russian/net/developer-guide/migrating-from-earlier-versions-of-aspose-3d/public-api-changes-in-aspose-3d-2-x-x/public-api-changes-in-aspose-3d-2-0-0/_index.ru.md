---
title: Публичные изменения API в Aspose.3D 2.0.0
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Содержание Резюме**

- [Добавляет формат Collada](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Добавляет Aspose.ThreeD. RenderTarget/IRenderTexture/IRenderWindow/ITextureUnit интерфейсы и Aspose.ThreeD.Render. Просмотр/ИнициализацияИсключение/Рендерер/Тип текстурИсключение водителя/Рендерклассы](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Добавляет класс Aspose.ThreeD.Render.PostProcessing](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Добавляет метод GetBoundingBox в класс Aspose.ThreeD.Node, Добавляет новые классы Aspose.ThreeD. Утилиты. BoundingBox и Aspose.ThreeD. Утилиты. BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Рендеринг в реальном времени](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [Методы AddData добавляются в класс Aspose.ThreeD. Entity. VertexElementUV](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 1.7.0 до 2.0.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Добавляет формат Collada**
В этой версии (2.0.0) разработчики могут импортировать файлы Collada 3D, поэтому свойство Collada добавляется в класс Aspose.ThreeD.FileFormat.
###  **Добавляет Aspose.ThreeD. RenderTarget/IRenderTexture/IRenderWindow/ITextureUnit интерфейсы и Aspose.ThreeD.Render. Просмотр/ИнициализацияИсключение/Рендерер/Тип текстурИсключение водителя/Рендерклассы**
Новые классы Viewport и Renderer являются основными классами, которые помогают захватывать виды сцены 3D и сохранять их в текстуре или окне. Все детали других классов помощи являются следующими:

- **Aspose.ThreeD. Рендер. Класс исключения водителя**-Исключения внутреннего рендерера обернуты как DriverException.
- **Aspose.ThreeD. Рендер. ИнициализацияКласс исключения**-Это исключение выбрасывается при неспособности инициализировать рендерер, например, инициализировать его на компьютере, который не имеет аппаратной поддержки OpenGL 4,0.
- **IRenderTarget интерфейс**-Это базовый интерфейс IRenderTexture/IRenderWindow.
- **Интерфейс IRenderTexture**-Он позволяет визуализировать сцену в одну или несколько текстур (текстуры расположены в видеопамяти и могут быть перенесены в системную память).
- **Интерфейс IRenderWindow**-Это позволяет визуализировать сцену в окно в режиме реального времени.
- **Интерфейс ITextureUnit**-ITextureUnit-это образец текстуры на стороне GPU и данные текстуры в памяти CPU или GPU.
- **Тип текстуры enum**-Он определяет тип текстур, таких как Texture1D, Texture2D, Texture3D, CubeMap и Array2D.
- **Класс RenderFactory**-Это помогает в рендеринге сцены в текстуры или окно в режиме реального времени.
- **Класс RenderParameters**-Он определяет параметры создания цели рендеринга, такие как цветовые биты, биты глубины, биты трафарета и двойная буферизация.

**Захват видовых экранов сцены 3D и рендеринг текстуры или окна**

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
###  **Добавляет класс Aspose.ThreeD.Render.PostProcessing**
Класс PostProcessing позволяет разработчикам применять фильтр обработки изображений в реальном времени к визуализированное изображение. В этой версии 2.0.0 мы предоставили 4 встроенных эффекта постобработки. Мы позволим разработчикам иметь собственный алгоритм постобработки в будущей версии.

**Применение визуальных эффектов при экономии 3D просмотров**

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
###  **Добавляет метод GetBoundingBox в класс Aspose.ThreeD.Node, Добавляет новые классы Aspose.ThreeD. Утилиты. BoundingBox и Aspose.ThreeD. Утилиты. BoundingBoxExtent**
Классы BoundingBox и BoundingBoxExtent представляют собой ограничительную рамку узла 3D. Разработчики могут сбросить камеру и рассчитать высоту от ограничивающей коробки. Бесконечная или нулевая ограничивающая коробка означает, что сцена не имеет геометрии и регулирует только высоту камеры, когда она конечна.
###  **Рендеринг в реальном времени**
Это позволяет разработчикам выполнять высокопроизводительный рендеринг в реальном времени на GUI-фреймворке, такой как WinForms, он не зависит от рамок GUI, поэтому другие фреймворки GUI также должны поддерживать это.
###  **Методы AddData добавляются в класс Aspose.ThreeD. Entity. VertexElementUV**
Базовый класс VertexElementUV изменился с VertexElementTemplate<Vector2>На VertexElementTemplate<Vector4>, Он будет хранить Vector4 только с 2.0.0, поэтому были добавлены два вспомогательных метода, чтобы позволить пользователю добавить список Vector2 и Vector3 в VertexElementUV, он внутренне расширит Vector2/Vector3 до Vector4 и оставит остальные поля равными нулю:
