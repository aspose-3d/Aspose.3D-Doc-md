+++
title = "Public API Changes in Aspose.3D 2.0.0" 
description = "" 
weight = 20083 
+++

Aspose.3D for .NET : Public API Changes in Aspose.3D 2.0.0  

# Aspose.3D for .NET : Public API Changes in Aspose.3D 2.0.0


{{< panel title="Contents Summary" style="primary" >}}
*   [Adds Collada format](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
*   [Adds Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit interfaces and Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParameters classes](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
*   [Adds Aspose.ThreeD.Render.PostProcessing class](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
*   [Adds GetBoundingBox method to Aspose.ThreeD.Node class, Adds new classes Aspose.ThreeD.Utilities.BoundingBox and Aspose.ThreeD.Utilities.BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
*   [Real-time Rendering](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
*   [AddData methods are added to Aspose.ThreeD.Entities.VertexElementUV class](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)
{{< /panel >}}
This document describes changes to the Aspose.3D API from version 1.7.0 to 2.0.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

### Adds Collada format

In this version (2.0.0), developers can import Collada 3D files, so the Collada property is added in Aspose.ThreeD.FileFormat class.

### Adds Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit interfaces and Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParameters classes

The new Viewport and Renderer classes are the main classes that helps to capture the views of a 3D scene and save to a texture or window. All details of other helping classes are as following:

*   **Aspose.ThreeD.Render.DriverException class** - the exceptions of the internal renderer are wrapped as DriverException.
*   **Aspose.ThreeD.Render.InitializationException class** - this exception is thrown while failing to initialize the renderer, for example to initialize it on a computer that has no hardware support of OpenGL 4.0.
*   **IRenderTarget interface** - It is the base interface of IRenderTexture/IRenderWindow.
*   **IRenderTexture interface** - It allows to render the scene to one or more textures (textures are located in video memory and can be transferred to system memory).
*   **IRenderWindow interface** - It allows to render the scene to window in real-time.
*   **ITextureUnit interface** - ITextureUnit is the texture sampler in GPU side and the texture data in CPU or GPU memory.
*   **TextureType enum** - It defines the type of textures, like Texture1D, Texture2D, Texture3D, CubeMap and Array2D.
*   **RenderFactory class** - It helps in rendering a scene to textures or window in real-time.
*   **RenderParameters class** - It defines the parameters about how to create the render target like color bits, depth bits, stencil bits and double buffering.

**Capture the Viewports of a 3D Scene and Render to a texture or window**

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

### Adds Aspose.ThreeD.Render.PostProcessing class

PostProcessing class allows developers to apply real-time image processing filter to the rendered image. In this version 2.0.0, we have provided 4 built-in post-processing effects. We'll allow developers to have their own custom post-processing algorithm in the future version.

**Apply Visual Effects on Saving 3D Views**

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

### Adds GetBoundingBox method to Aspose.ThreeD.Node class, Adds new classes Aspose.ThreeD.Utilities.BoundingBox and Aspose.ThreeD.Utilities.BoundingBoxExtent

The BoundingBox and BoundingBoxExtent classes represent bounding box of a 3D node. Developers may reset the camera, and calculate the elevation from bounding box. The infinite or null bounding box means the scene has no geometries and only adjust camera's elevation when it's finite.

### Real-time Rendering

It allows developers to perform high-performance real-time rendering on a GUI framework like WinForms, it's GUI framework-independent, so the other GUI frameworks should also support this.

### AddData methods are added to Aspose.ThreeD.Entities.VertexElementUV class

The VertexElementUV's base class has changed from VertexElementTemplate<Vector2> to VertexElementTemplate<Vector4>, it will only store Vector4 since 2.0.0, so two helper methods were added to allow user to add a list of Vector2 and Vector3 to VertexElementUV, it will internally expand the Vector2/Vector3 to Vector4 and leave the rest fields zero:

