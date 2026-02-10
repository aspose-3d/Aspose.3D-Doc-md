---
title: Appliquer des effets visuels sur les vues de Saving 3D
type: docs
weight: 10
url: /fr/net/apply-visual-effects-on-saving-3d-views/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent appliquer des effets visuels sur les vues 3D avant de les enregistrer dans l'image. Ces effets visuels sont également connus sous le nom d'effets de post-traitement ou de filtres qui sont appliqués en temps réel à tout ce qui est affiché dans la vue 3D.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), les développeurs peuvent appliquer des effets visuels sur les vues 3D avant d'enregistrer dans l'image. Ces effets visuels sont également connus comme les effets de post-traitement ou les filtres qui sont appliqués en temps réel à tout ce qui s'affiche dans la vue 3D.

{{% /alert %}}
##  **Appliquer des effets visuels sur 3D Voir**
La méthode [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) de la classe [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) permet de créer n'importe quel effet visuel pris en charge. La classe Renderer offre un membre [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) pour appliquer différents filtres, la méthode Add de la classe PostProcessings permet d'incorporer un filtre avant le rendu.
###  **Échantillon de programmation**
Cet exemple de code applique un effet visuel sur une vue 3D.

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
