---
title: Rendre 3D Voir au format Image depuis la caméra
type: docs
weight: 50
url: /fr/python-net/render-3d-view-in-image-format-from-camera/
description: En utilisant Aspose.3D for Python via .NET, les développeurs peuvent rendre une image pour afficher une image réaliste du modèle 3D, avec ou sans le fond amélioré, les textures, les ombres et également ajuster la taille de l'image.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), les développeurs peuvent rendre une image pour afficher une image réaliste du modèle 3D, avec ou sans le fond amélioré, les textures, les ombres et également ajuster la taille de l'image.

{{% /alert %}}
##  **Prenez une photo du modèle de 3D de l'appareil photo**
La méthode Render exposée par la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) peut être utilisée pour prendre une photo à partir de la caméra active. Les développeurs peuvent également utiliser les différentes façons de naviguer et de positionner la caméra dans la scène. Dans cet exemple de code, nous créons une caméra à la position (10,10,10) dans une scène 3D existante et regardons le point d'origine pour le rendu.
###  **Échantillon de programmation**
Cet exemple de code crée une caméra dans une scène 3D, définit sa cible et rend une image.

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
