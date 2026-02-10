---
title: Рендер 3D Просмотр в формате изображения с камеры
type: docs
weight: 50
url: /ru/net/render-3d-view-in-image-format-from-camera/
description: Используя Aspose.3D for .NET, разработчики могут отрисовывать изображение для просмотра реалистичного изображения модели 3D с улучшенным фоном, текстурами, тенями или без них, а также настраивать размер изображения.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики могут визуализировать изображение для просмотра реалистичного изображения модели 3D с улучшенным фоном, текстурами, тенями или без них, а также настраивать размер изображения.

{{% /alert %}}
##  **Сделайте снимок модели 3D с камеры**
Метод `Render`, представленный классом [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), можно использовать для получения снимка с активной камеры. Разработчики также могут использовать несколько различных способов навигации и позиционирования камеры в сцене. В этом примере кода мы создаем камеру в позиции (10,10,10) в существующей сцене 3D и смотрим на исходную точку для рендеринга.
###  **Образец программирования**
Этот пример кода создает камеру в сцене 3D, устанавливает ее цель и визуализирует изображение.

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
