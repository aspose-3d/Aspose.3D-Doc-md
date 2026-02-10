---
title: Changing Plane Orientation
type: docs
weight: 40
url: /python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET allows changing orientation of a scene. In order to change the orientation, Up vector property is introduced in Plane Class.
---

# **Changing Plane Orientation**
Aspose.3D for Python via .NET allows changing orientation of a scene. In order to change the orientation, `up` vector property is introduced in `Plane` Class. Following code snippet shows how to change to plane's orientation:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Plane
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the data directory.
dataDir = "data-dir"
#  Initialize scene object
scene = Scene()
plane = Plane()
plane.up = Vector3(1, 1, 3)
#  Set Vector
scene.root_node.create_child_node(plane)
#  This will generate a plane that has customized orientation
scene.save(dataDir + "ChangePlaneOrientation.obj", FileFormat.WAVEFRONT_OBJ)
{{< /highlight >}}
