---
title: Render 3D Ver en formato de imagen desde la cámara
type: docs
weight: 50
url: /es/python-net/render-3d-view-in-image-format-from-camera/
description: Usando Aspose.3D for Python via .NET, los desarrolladores pueden renderizar una imagen para ver una imagen realista del modelo 3D, con o sin el fondo mejorado, las texturas, las sombras y también ajustar el tamaño de la imagen.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), los desarrolladores pueden renderizar una imagen para ver una imagen realista del modelo 3D, con o sin el fondo mejorado, las texturas, las sombras y también ajustar el tamaño de la imagen.

{{% /alert %}}
##  **Tome una foto del modelo 3D desde la cámara**
El método Render expuesto por la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) se puede utilizar para tomar una fotografía desde la cámara activa. Los desarrolladores también pueden usar las diferentes formas de navegar y posicionar la cámara en la escena. En este ejemplo de código, creamos una cámara en la posición (10,10,10) en una escena 3D existente y observamos el punto de origen para renderizar.
###  **Muestra de programación**
Este ejemplo de código crea una cámara en una escena 3D, establece su objetivo y renderizar una imagen.

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
