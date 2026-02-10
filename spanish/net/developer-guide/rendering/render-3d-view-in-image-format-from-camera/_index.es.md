---
title: Render 3D Ver en formato de imagen desde la cámara
type: docs
weight: 50
url: /es/net/render-3d-view-in-image-format-from-camera/
description: Usando Aspose.3D for .NET, los desarrolladores pueden renderizar una imagen para ver una imagen realista del modelo 3D, con o sin el fondo mejorado, las texturas, las sombras y también ajustar el tamaño de la imagen.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden renderizar una imagen para ver una imagen realista del modelo 3D, con o sin el fondo mejorado, las texturas, las sombras y también ajustar el tamaño de la imagen.

{{% /alert %}}
##  **Tome una foto del modelo 3D desde la cámara**
El método `Render` expuesto por la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) se puede utilizar para tomar una fotografía de la cámara activa. Los desarrolladores también pueden usar las diferentes formas de navegar y posicionar la cámara en la escena. En este ejemplo de código, creamos una cámara en la posición (10,10,10) en una escena 3D existente y observamos el punto de origen para la representación.
###  **Muestra de programación**
Este ejemplo de código crea una cámara en una escena 3D, establece su objetivo y renderizar una imagen.

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
