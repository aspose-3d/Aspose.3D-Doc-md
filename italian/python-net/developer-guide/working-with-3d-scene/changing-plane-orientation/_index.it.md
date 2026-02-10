---
title: Cambiamento dell'orientamento aereo
type: docs
weight: 40
url: /it/python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET consente di modificare l'orientamento di una scena. Per modificare l'orientamento, la proprietà vettore Up viene introdotta in Classe aereo.
---
#  **Cambiamento dell'orientamento aereo**
Aspose.3D for Python via .NET consente di modificare l'orientamento di una scena. Per modificare l'orientamento, la proprietà vettoriale `up` viene introdotta nella classe `Plane`. Il seguente frammento di codice mostra come modificare l'orientamento dell'aereo:

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
