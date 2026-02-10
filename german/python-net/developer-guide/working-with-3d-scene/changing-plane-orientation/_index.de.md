---
title: Veränderung der Flugzeug orientierung
type: docs
weight: 40
url: /de/python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET ermöglicht die Änderung der Ausrichtung einer Szene. Um die Ausrichtung zu ändern, wird die Up-Vektor-Eigenschaft in der Flugzeug klasse eingeführt.
---
#  **Veränderung der Flugzeug orientierung**
Aspose.3D for Python via .NET ermöglicht die Änderung der Ausrichtung einer Szene. Um die Ausrichtung zu ändern, wird die `up`-Vektor eigenschaft in der `Plane`-Klasse eingeführt. Das folgende Code-Snippet zeigt, wie die Ausrichtung des Flugzeugs geändert wird:

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
