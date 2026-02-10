---
title: 在保存 3D 个视图时应用视觉效果
type: docs
weight: 10
url: /zh/net/apply-visual-effects-on-saving-3d-views/
description: 使用 Aspose.3D for .NET API，开发人员可以在保存到图像之前对 3D 视图应用视觉效果。这些视觉效果也称为后处理效果或滤镜，它们实时应用于 3D 视图中显示的所有内容。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET API](https://products.aspose.com/3d/net/)，开发人员可以在保存到图像之前对 3D 视图应用视觉效果。这些视觉效果也称为后处理效果或过滤器，它们实时应用于 3D 视图中显示的所有内容。

{{% /alert %}}
##  **在 3D 视图上应用视觉效果**
[`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) 类的 [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) 方法允许创建任何受支持的视觉效果。Renderer类提供了一个 [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) 成员来应用各种过滤器，PostProcessings类的Add方法允许在呈现之前合并一个过滤器。
###  **编程示例**
此代码示例对 3D 视图应用视觉效果。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D scene
Scene scene = Scene.FromFile("scene.obj");
// Create an instance of the camera
Camera camera = new Camera();
scene.RootNode.CreateChildNode("camera", camera).Transform.Translation = new Vector3(2, 44, 66);
// Set the target
camera.LookAt = new Vector3(50, 12, 0);
// Create a light
scene.RootNode.CreateChildNode("light", new Light() { Color = new Vector3(Color.White), LightType = LightType.Point }).Transform.Translation = new Vector3(26, 57, 43);

// The CreateRenderer will create a hardware OpenGL-backend renderer, more renderer will be added in the future
// And some internal initializations will be done.
// When the renderer left using the scope, the unmanaged hardware resources will also be disposed
using (var renderer = Renderer.CreateRenderer())
{
    renderer.EnableShadows = false;

    // Create a new render target that renders the scene to texture(s)
    // Use default render parameters
    // And one output targets
    // Size is 1024 x 1024
    // This render target can have multiple render output textures, but here we only need one output.
    // The other textures and depth textures are mainly used by deferred shading in the future.
    // But you can also access the depth texture through IRenderTexture.DepthTeture
    using (IRenderTexture rt = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(), 1, 1024, 1024))
    {
        // This render target has one viewport to render, the viewport occupies the 100% width and 100% height
        Viewport vp = rt.CreateViewport(camera, new RelativeRectangle() { ScaleWidth = 1, ScaleHeight = 1 });
        // Render the target and save the target texture to external file
        renderer.Render(rt);
        ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("Original_viewport_out.png"), ImageFormat.Png);

        // Create a post-processing effect
        PostProcessing pixelation = renderer.GetPostProcessing("pixelation");
        renderer.PostProcessings.Add(pixelation);
        renderer.Render(rt);
        ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("VisualEffect_pixelation_out.png"), ImageFormat.Png);

        // Clear previous post-processing effects and try another one
        PostProcessing grayscale = renderer.GetPostProcessing("grayscale");
        renderer.PostProcessings.Clear();
        renderer.PostProcessings.Add(grayscale);
        renderer.Render(rt);
        ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("VisualEffect_grayscale_out.png"), ImageFormat.Png);

        // We can also combine post-processing effects
        renderer.PostProcessings.Clear();
        renderer.PostProcessings.Add(grayscale);
        renderer.PostProcessings.Add(pixelation);
        renderer.Render(rt);
        ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("VisualEffect_grayscale+pixelation_out.png"), ImageFormat.Png);

        // Clear previous post-processing effects and try another one
        PostProcessing edgedetection = renderer.GetPostProcessing("edge-detection");
        renderer.PostProcessings.Clear();
        renderer.PostProcessings.Add(edgedetection);
        renderer.Render(rt);
        ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("VisualEffect_edgedetection_out.png"), ImageFormat.Png);

        // Clear previous post-processing effects and try another one
        PostProcessing blur = renderer.GetPostProcessing("blur");
        renderer.PostProcessings.Clear();
        renderer.PostProcessings.Add(blur);
        renderer.Render(rt);
        ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("VisualEffect_blur_out.png"), ImageFormat.Png);
    }
}

{{< /highlight >}}
