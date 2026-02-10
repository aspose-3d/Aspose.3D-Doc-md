---
title: Visualizza 3D in formato immagine dalla fotocamera
type: docs
weight: 50
url: /it/net/render-3d-view-in-image-format-from-camera/
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono eseguire il rendering di un'immagine per visualizzare un'immagine realistica del modello 3D, con o senza lo sfondo, le trame e le ombre migliorate e anche regolare le dimensioni dell'immagine.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono eseguire il rendering di un'immagine per visualizzare un'immagine realistica del modello 3D, con o senza lo sfondo, le trame e le ombre migliorate e anche regolare le dimensioni dell'immagine.

{{% /alert %}}
##  **Scatta una foto del modello 3D dalla fotocamera**
Il metodo `Render` esposto dalla classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) può essere utilizzato per scattare una foto dalla fotocamera attiva. Gli sviluppatori possono anche utilizzare diversi modi per navigare e posizionare la telecamera nella scena. In questo esempio di codice, creiamo una fotocamera in posizione (10,10,10) in una scena esistente di 3D e guardiamo il punto di origine per il rendering.
###  **Campione di programmazione**
Questo esempio di codice crea una fotocamera in una scena 3D, imposta la sua destinazione e rende un'immagine.

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
