---
title: Render 3D Ansicht im Bildformat von der Kamera
type: docs
weight: 50
url: /de/python-net/render-3d-view-in-image-format-from-camera/
description: Mit Aspose.3D for Python via .NET können Entwickler ein Bild rendern, um ein realistisches Bild des 3D-Modells mit oder ohne erweiterten Hintergrund, Texturen und Schatten anzuzeigen und auch die Bildgröße anzupassen.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) können Entwickler ein Bild rendern, um ein realistisches Bild des 3D-Modells mit oder ohne erweiterten Hintergrund, Texturen und Schatten anzuzeigen und auch die Bildgröße anzupassen.

{{% /alert %}}
##  **Machen Sie ein Bild von 3D Modell von der Kamera**
Die Render-Methode, die von der [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse verfügbar gemacht wird, kann verwendet werden, um ein Bild von der aktiven Kamera aufzunehmen. Entwickler können auch verschiedene Möglichkeiten verwenden, um die Kamera in der Szene zu navigieren und zu positionieren. In diesem Code beispiel erstellen wir eine Kamera an Position (10,10,10) in einer vorhandenen 3D-Szene und betrachten den Ursprungs punkt zum Rendern.
###  **Programmier probe**
Dieses Code beispiel erstellt eine Kamera in einer 3D-Szene, legt ihr Ziel fest und rendert ein Bild.

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
