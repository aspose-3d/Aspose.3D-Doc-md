---
title: Aspose 中的公共 API 更改。3D 2.0.0
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-3d-2-0-0/
---
**内容摘要**

- [添加 Collada 格式](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [添加 Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit接口和 Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParameters类](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [添加 Aspose.ThreeD.Render.PostProcessing类](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [将GetBoundingBox方法添加到 Aspose.ThreeD.Node类，添加新类 Aspose.ThreeD.Utilities.BoundingBox和 Aspose.ThreeD.Utilities.BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [实时渲染](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [AddData方法被添加到 Aspose.ThreeD.Entities.VertexElementUV类](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本1.7.0到2.0.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **添加 Collada 格式**
在此版本 (2.0.0) 中，开发人员可以导入 Collada 3D 文件，因此 Collada 属性被添加到 Aspose.ThreeD.FileFormat类中。
###  **添加 Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit接口和 Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParameters类**
新的视口和渲染器类是帮助捕获 3D 场景视图并保存到纹理或窗口的主要类。其他帮助类的所有细节如下:

- **Aspose.ThreeD.Render.DriverException类**-内部渲染器的异常被包装为DriverException。
- **Aspose.ThreeD.Render.InitializationException类**-在无法初始化渲染器 (例如在不支持OpenGL 4.0的硬件的计算机上初始化渲染器) 时引发此异常。
- **IRenderTarget接口**-它是IRenderTexture/IRenderWindow的基础接口。
- **IRenderTexture接口**-它允许将场景渲染为一个或多个纹理 (纹理位于视频存储器中，可以传输到系统存储器中)。
- **IRenderWindow接口**-它允许将场景实时渲染到窗口。
- **ITextureUnit接口**-ITextureUnit是GPU侧的纹理采样器，是CPU或GPU内存中的纹理数据。
- **纹理类型枚举**-它定义纹理的类型，如Texture1D，Texture2D，Texture3D，CubeMap和Array2D。
- **RenderFactory类**-它有助于将场景实时渲染为纹理或窗口。
- **RenderParameters类**-它定义了有关如何创建渲染目标的参数，例如颜色位，深度位，模板位和双重缓冲。

**捕获 3D 场景的视口并渲染到纹理或窗口**

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
###  **添加 Aspose.ThreeD.Render.PostProcessing类**
后处理类允许开发人员将实时图像处理过滤器应用于渲染的图像。在此版本2.0.0中，我们提供了4个内置的后处理效果。我们将允许开发人员在将来的版本中拥有自己的自定义后处理算法。

**在保存 3D 个视图时应用视觉效果**

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
###  **将GetBoundingBox方法添加到 Aspose.ThreeD.Node类，添加新类 Aspose.ThreeD.Utilities.BoundingBox和 Aspose.ThreeD.Utilities.BoundingBoxExtent**
BoundingBox和BoundingBoxExtent类表示 3D 节点的边界框。开发人员可以重置相机，并从边界框计算高程。无限或空边界框意味着场景没有几何图形，只有在有限的情况下才调整摄影机的高程。
###  **实时渲染**
它允许开发人员在像WinForms这样的GUI框架上执行高性能实时渲染，它与GUI框架无关，因此其他GUI框架也应该支持这一点。
###  **AddData方法被添加到 Aspose.ThreeD.Entities.VertexElementUV类**
VertexElementUV的基类已从VertexElementTemplate更改<Vector2>到VertexElementTemplate<Vector4>,它将仅从2.0.0开始存储Vector4，因此添加了两个帮助方法以允许用户将Vector2和Vector3的列表添加到VertexElementUV，它将在内部将Vector2/Vector3扩展到Vector4并将其余字段保持为零:
