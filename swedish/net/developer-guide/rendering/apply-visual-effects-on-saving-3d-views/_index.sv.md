---
title: Använd visuella effekter vid sparning av 3D Visningar
type: docs
weight: 10
url: /sv/net/apply-visual-effects-on-saving-3d-views/
description: Använder Aspose. 3D for .NET API, utvecklare kan använda visuella effekter på 3D vyer innan bilden sparas. Dessa visuella effekter kallas också de efterbehandlingseffekter eller filter som används i realtid för allt som visas i 3D Visa.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET API](https://products.aspose.com/3d/net/) kan utvecklare använda visuella effekter på 3D vyer innan bilden sparas. Dessa visuella effekter kallas också de efterbehandlingseffekter eller filter som används i realtid för allt som visas i 3D Visa.

{{% /alert %}}
##  **Använd visuella effekter på 3D Visa**
[`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)-metoden för [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)-klassen gör det möjligt att skapa en visuell effekt som stöds. Klassen Renderer erbjuder en [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)-medlem för att applicera olika filter, Tilläggsmetoden i Postprocessing-klassen gör det möjligt att inkorporera ett filter innan återgivning.
###  **Programmeringsprova**
Det här kodexemplet gäller visuell effekt på en 3D-vy.

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
