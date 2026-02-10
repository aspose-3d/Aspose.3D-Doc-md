---
title: Rendera 3D Visa i bildformat från kameran
type: docs
weight: 50
url: /sv/net/render-3d-view-in-image-format-from-camera/
description: Använder Aspose. 3D for .NET, kan utvecklare göra en bild för att visa en realistisk bild av 3D-modell, med eller utan den förbättrade bakgrunden, texturer, skuggor och även justera bildstorleken.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare visa en bild för att visa en realistisk bild av 3D-modell, med eller utan den förbättrade bakgrunden, texturer, skuggor och justera bildstorleken.

{{% /alert %}}
##  **Ta en bild av 3D Modell från kameran**
Metoden `Render` som exponeras av klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) kan användas för att ta en bild från den aktiva kameran. Utvecklare kan också använda flera olika sätt att navigera och placera kameran i scenen. I detta kodexempel skapar vi en kamera i position (10,10,10) i en befintlig 3D-scen och titta på ursprungspunkten för rendering.
###  **Programmeringsprova**
Det här kodexemplet skapar en kamera i en 3D-scen, ställer in målet och visar en bild.

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
