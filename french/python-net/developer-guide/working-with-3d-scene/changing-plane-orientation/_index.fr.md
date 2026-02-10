---
title: Changer l'orientation de l'avion
type: docs
weight: 40
url: /fr/python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET permet de changer l'orientation d'une scène. Pour modifier l'orientation, la propriété de vecteur Up est introduite dans Plane Class.
---
#  **Changer l'orientation de l'avion**
Aspose.3D for Python via .NET permet de changer l'orientation d'une scène. Pour changer l'orientation, la propriété de vecteur `up` est introduite dans la classe `Plane`. L'extrait de code suivant montre comment modifier l'orientation du plan:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Plane
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the data directory
dataDir = "data-dir"
#  Initialize scene object
scene = Scene()
plane = Plane()
plane.up = Vector3(1, 1, 3)
#  Set Vector
scene.root_node.create_child_node(plane)
# This will generate a plane that has customized orientation
scene.save(dataDir + "ChangePlaneOrientation.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
