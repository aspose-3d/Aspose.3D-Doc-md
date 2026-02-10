---
title: 捕获 3D 场景的视口并渲染到纹理或窗口
type: docs
weight: 20
url: /zh/net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: 每个 3D 场景可以包含任意数量的视口。使用 Aspose.3D for .NET API，开发人员可以在单个屏幕截图中捕获一个或多个视口。他们可以在基于GUI的 .NET 应用程序或图像中呈现它。
---
{{% alert color="primary" %}}

每个 3D 场景可以包含任意数量的视口。使用 [Aspose.3D for .NET API](https://products.aspose.com/3d/net/)，开发人员可以在单个屏幕截图中捕获一个或多个视口。他们可以在基于GUI的 .NET 应用程序或图像中呈现它。

{{% /alert %}}
##  **捕获和渲染 3D 场景的视口**
[`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) 类公开的 `CreateRenderTexture` 和 `CreateRenderWindow` 方法可用于创建将场景渲染到纹理或窗口的新渲染目标。
###  **编程示例**
此代码示例捕获 3D 场景的视口，并以两种不同的方式呈现它。

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

            // The CreateRenderer will create a hardware OpenGL-backend renderer
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
                // Use CreateRenderWindow method to render in window, like:
                // Window = renderer.RenderFactory.CreateRenderWindow(new RenderParameters(), Handle);
                using (IRenderTexture rt = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(), 1, 1024, 1024))
                {
                    // This render target has one viewport to render, the viewport occupies the 100% width and 100% height
                    Viewport vp = rt.CreateViewport(camera, new RelativeRectangle() { ScaleWidth = 1, ScaleHeight = 1 });
                    // Render the target and save the target texture to external file
                    renderer.Render(rt);
                    ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("file-1viewports_out.png"), ImageFormat.Png);

                    // Now let's change the previous viewport only uses the half left side(50% width and 100% height)
                    vp.Area = new RelativeRectangle() { ScaleWidth = 0.5f, ScaleHeight = 1 };
                    // And create a new viewport that occupies the 50% width and 100% height and starts from 50%
                    // Both of them are using the same camera, so the rendered content should be the same
                    rt.CreateViewport(camera, new RelativeRectangle() { ScaleX = 0.5f, ScaleWidth = 0.5f, ScaleHeight = 1 });
                    // But this time let's increase the field of view of the camera to 90 degree so it can see more part of the scene
                    camera.FieldOfView = 90;
                    renderer.Render(rt);
                    ((ITexture2D)rt.Targets[0]).Save(RunExamples.GetOutputFilePath("file-2viewports_out.png"), ImageFormat.Png);
                }
            }

{{< /highlight >}}
