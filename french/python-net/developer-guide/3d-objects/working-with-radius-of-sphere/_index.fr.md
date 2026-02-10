---
title: Travailler avec le rayon de la sphère
type: docs
weight: 110
url: /fr/python-net/working-with-radius-of-sphere/
description: En utilisant Aspose.3D for Python via .NET, vous pouvez définir le rayon get d'une sphère. Pour obtenir ou définir un rayon, vous pouvez utiliser la propriété Radius de la classe Sphere. Voici l'exemple de code pour définir le rayon d'une sphère.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.4 ou supérieure.

{{% /alert %}} 
##  **Travail avec rayon de sphère**
En utilisant Aspose.3D for Python via .NET, vous pouvez définir le rayon get d'une sphère. Pour obtenir ou définir radius, vous pouvez utiliser la propriété `radius` de la classe `Sphere`. Voici l'exemple de code pour définir le rayon d'une sphère.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
sphere = Sphere()
sphere.radius = 10 .0
#  Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.root_node.create_child_node(sphere)
#  Save scene
scene.save("data-dir"  + "sphere.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
