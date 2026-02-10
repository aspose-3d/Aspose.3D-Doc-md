---
title: Visualizza 3D in formato immagine dalla fotocamera
type: docs
weight: 50
url: /it/python-net/render-3d-view-in-image-format-from-camera/
description: Utilizzando Aspose.3D for Python via .NET, gli sviluppatori possono eseguire il rendering di un'immagine per visualizzare un'immagine realistica del modello 3D, con o senza lo sfondo, le trame e le ombre migliorate e anche regolare le dimensioni dell'immagine.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), gli sviluppatori possono eseguire il rendering di un'immagine per visualizzare un'immagine realistica del modello 3D, con o senza lo sfondo, le trame e le ombre migliorate e anche regolare le dimensioni dell'immagine.

{{% /alert %}}
##  **Scatta una foto del modello 3D dalla fotocamera**
Il metodo Render esposto dalla classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) può essere utilizzato per scattare una foto dalla fotocamera attiva. Gli sviluppatori possono anche utilizzare diversi modi per navigare e posizionare la telecamera nella scena. In questo esempio di codice, creiamo una fotocamera in posizione (10,10,10) in una scena esistente di 3D e guardiamo il punto di origine per il rendering.
###  **Campione di programmazione**
Questo esempio di codice crea una fotocamera in una scena 3D, imposta la sua destinazione e rende un'immagine.

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
