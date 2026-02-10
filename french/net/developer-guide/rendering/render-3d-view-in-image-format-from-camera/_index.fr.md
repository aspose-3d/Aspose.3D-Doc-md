---
title: Rendre 3D Voir au format Image depuis la caméra
type: docs
weight: 50
url: /fr/net/render-3d-view-in-image-format-from-camera/
description: En utilisant Aspose.3D for .NET, les développeurs peuvent rendre une image pour afficher une image réaliste du modèle 3D, avec ou sans l'arrière-plan, les textures, les ombres améliorés et également ajuster la taille de l'image.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent rendre une image pour afficher une image réaliste du modèle 3D, avec ou sans le fond amélioré, les textures, les ombres et également ajuster la taille de l'image.

{{% /alert %}}
##  **Prenez une photo du modèle de 3D de l'appareil photo**
La méthode `Render` exposée par la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) peut être utilisée pour prendre une photo de la caméra active. Les développeurs peuvent également utiliser les différentes façons de naviguer et de positionner la caméra dans la scène. Dans cet exemple de code, nous créons une caméra à la position (10,10,10) dans une scène 3D existante et regardons le point d'origine pour le rendu.
###  **Échantillon de programmation**
Cet exemple de code crée une caméra dans une scène 3D, définit sa cible et rend une image.

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
