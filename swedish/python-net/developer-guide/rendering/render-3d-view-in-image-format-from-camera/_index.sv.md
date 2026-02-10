---
title: Rendera 3D Visa i bildformat från kameran
type: docs
weight: 50
url: /sv/python-net/render-3d-view-in-image-format-from-camera/
description: Med Aspose.3D for Python via .NET kan utvecklare visa en bild för att visa en realistisk bild av 3D-modell, med eller utan den förbättrade bakgrunden, texturer, skuggor och justera bildstorleken.
---
{{% alert color="primary" %}}

Med [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) kan utvecklare visa en bild för att visa en realistisk bild av 3D-modell, med eller utan den förbättrade bakgrunden, texturer, skuggor och justera bildstorleken.

{{% /alert %}}
##  **Ta en bild av 3D Modell från kameran**
Metoden Render som exponeras av klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) kan användas för att ta en bild från den aktiva kameran. Utvecklare kan också använda flera olika sätt att navigera och placera kameran i scenen. I detta kodexempel skapar vi en kamera i position (10,10,10) i en befintlig 3D-scen och titta på ursprungspunkten för rendering.
###  **Programmeringsprova**
Det här kodexemplet skapar en kamera i en 3D-scen, ställer in målet och visar en bild.

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
