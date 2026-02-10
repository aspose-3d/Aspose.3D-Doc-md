---
title: Render 3D View in Image format from Camera
type: docs
weight: 50
url: /python-net/render-3d-view-in-image-format-from-camera/
description: Using Aspose.3D for Python via .NET, developers can render an image to view a realistic image of 3D model, with or without the enhanced background, textures, shadows and also adjust the image size.
---

{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), developers can render an image to view a realistic image of 3D model, with or without the enhanced background, textures, shadows and also adjust the image size.

{{% /alert %}}
## **Take a Picture of 3D Model from the Camera**
The Render method exposed by the [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class can be used to take a picture from the active camera. Developers may also use the several different ways to navigate and position the camera in the scene. In this code example, we create a camera at position (10,10,10) in an existing 3D scene and look at the origin point for rendering.
### **Programming Sample**
This code example creates a camera in a 3D scene, sets its target and render an image.

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
