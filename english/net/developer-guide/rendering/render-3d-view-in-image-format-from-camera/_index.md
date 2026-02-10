---
title: Render 3D View in Image format from Camera
type: docs
weight: 50
url: /net/render-3d-view-in-image-format-from-camera/
description: Using Aspose.3D for .NET, developers can render an image to view a realistic image of 3D model, with or without the enhanced background, textures, shadows and also adjust the image size.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can render an image to view a realistic image of 3D model, with or without the enhanced background, textures, shadows and also adjust the image size.

{{% /alert %}}
## **Take a Picture of 3D Model from the Camera**
The `Render` method exposed by the [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class can be used to take a picture from the active camera. Developers may also use the several different ways to navigate and position the camera in the scene. In this code example, we create a camera at position (10,10,10) in an existing 3D scene and look at the origin point for rendering.
### **Programming Sample**
This code example creates a camera in a 3D scene, sets its target and render an image.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

                // Load scene from file
                Scene scene =  Scene.FromFile("camera.usdz");
                // Create a camera at (10,10,10) and look at the origin point for rendering,
                // It must be attached to the scene before render
                Camera camera = new Camera();
                scene.RootNode.CreateChildNode("camera", camera);
                camera.ParentNode.Transform.Translation = new Vector3(10, 10, 10);
                camera.LookAt = Vector3.Origin;

                // Specify the image render option
                ImageRenderOptions opt = new ImageRenderOptions();
                // Set the background color
                opt.BackgroundColor = Color.AliceBlue;
                // Tells renderer where the it can find textures
                opt.AssetDirectories.Add("textures");
                // Turn on shadow
                opt.EnableShadows = true;
                // Render the scene in given camera's perspective into specified png file with size 1024x1024
                scene.Render(camera, "Render3DModelImageFromCamera.png", new Size(1024, 1024), ImageFormat.Png, opt);

{{< /highlight >}}
