---
title: Kameradan görüntü biçiminde 3D görünümü
type: docs
weight: 50
url: /tr/python-net/render-3d-view-in-image-format-from-camera/
description: Aspose.3D for Python via .NET kullanarak, geliştiriciler gelişmiş arka plan, dokular, gölgeler ile veya olmadan 3D modelinin gerçekçi bir görüntüsünü görüntülemek için bir görüntü oluşturabilir ve ayrıca görüntü boyutunu ayarlayabilir.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) kullanarak, geliştiriciler gelişmiş arka plan, dokular, gölgeler ile veya olmadan 3D modelinin gerçekçi bir görüntüsünü görüntülemek için bir görüntü oluşturabilir ve ayrıca görüntü boyutunu ayarlayabilir.

{{% /alert %}}
##  **Kameradan 3D modelinin resmini çekin**
The Render method exposed by the [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class can be used to take a picture from the active camera. Developers may also use the several different ways to navigate and position the camera in the scene. In this code example, we create a camera at position (10,10,10) in an existing 3D scene and look at the origin point for rendering.
###  **Programming ample ample**
Bu kod örneği, 3D sahnesinde bir kamera oluşturur, hedefini ayarlar ve bir görüntü oluşturur.

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
