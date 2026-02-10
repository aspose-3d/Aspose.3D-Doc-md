---
title: Рендер 3D Просмотр в формате изображения с камеры
type: docs
weight: 50
url: /ru/python-net/render-3d-view-in-image-format-from-camera/
description: Используя Aspose.3D for Python via .NET, разработчики могут визуализировать изображение для просмотра реалистичного изображения модели 3D с улучшенным фоном, текстурами, тенями или без них, а также настраивать размер изображения.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), разработчики могут визуализировать изображение для просмотра реалистичного изображения модели 3D с улучшенным фоном, текстурами, тенями или без них, а также настраивать размер изображения.

{{% /alert %}}
##  **Сделайте снимок модели 3D с камеры**
Метод Render, представленный классом [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), может использоваться для получения снимка с активной камеры. Разработчики также могут использовать несколько различных способов навигации и позиционирования камеры в сцене. В этом примере кода мы создаем камеру в позиции (10,10,10) в существующей сцене 3D и смотрим на исходную точку для рендеринга.
###  **Образец программирования**
Этот пример кода создает камеру в сцене 3D, устанавливает ее цель и визуализирует изображение.

{{< highlight "python" >}}
from aspose.pydrawing import Color, Size
from aspose.pydrawing.imaging import ImageFormat
from aspose.threed import ImageRenderOptions, Scene
from aspose.threed.entities import Camera
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load scene from file
scene = Scene("data-dir"  + "camera.3ds")
#  Create a camera at (10,10,10) and look at the origin point for rendering,
#  It must be attached to the scene before render
camera = Camera()
scene.root_node.create_child_node("camera", camera)
camera.parent_node.transform.translation = Vector3(10, 10, 10)
camera.look_at = Vector3.ORIGIN
#  Specify the image render option
opt = ImageRenderOptions()
#  Set the background color
opt.background_color = Color.alice_blue
#  Tells renderer where the it can find textures
opt.asset_directories.append("data-dir"  + "textures")
#  Turn on shadow
opt.enable_shadows = True
#  Render the scene in given camera's perspective into specified png file with size 1024x1024
scene.render(camera, "out"  + "Render3DModelImageFromCamera.png", Size(1024, 1024), ImageFormat.png, opt)

{{< /highlight >}}
