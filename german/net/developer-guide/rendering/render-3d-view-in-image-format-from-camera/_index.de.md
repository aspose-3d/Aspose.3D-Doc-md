---
title: Render 3D Ansicht im Bildformat von der Kamera
type: docs
weight: 50
url: /de/net/render-3d-view-in-image-format-from-camera/
description: Mit Aspose.3D for .NET können Entwickler ein Bild rendern, um ein realistisches Bild des 3D-Modells mit oder ohne erweiterten Hintergrund, Texturen und Schatten anzuzeigen und auch die Bildgröße anzupassen.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler ein Bild rendern, um ein realistisches Bild des 3D-Modells mit oder ohne erweiterten Hintergrund, Texturen und Schatten anzuzeigen und auch die Bildgröße anzupassen.

{{% /alert %}}
##  **Machen Sie ein Bild von 3D Modell von der Kamera**
Die `Render`-Methode, die von der [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse verfügbar ist, kann verwendet werden, um ein Bild von der aktiven Kamera aufzunehmen. Entwickler können auch verschiedene Möglichkeiten verwenden, um die Kamera in der Szene zu navigieren und zu positionieren. In diesem Code beispiel erstellen wir eine Kamera an Position (10,10,10) in einer vorhandenen 3D-Szene und betrachten den Ursprungs punkt zum Rendern.
###  **Programmier probe**
Dieses Code beispiel erstellt eine Kamera in einer 3D-Szene, legt ihr Ziel fest und rendert ein Bild.

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
