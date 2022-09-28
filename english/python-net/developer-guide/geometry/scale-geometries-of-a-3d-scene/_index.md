---
title: Scale geometries of a 3D Scene
type: docs
weight: 70
url: /python-net/scale-geometries-of-a-3d-scene/
description: Developers can scale only geometries of a 3D node or all nodes of 3D Scene. In order to achieve this, developers can call multiple Scale members of the PolygonModifier class instance.
---

## **Scale geometries of a single 3D node or all nodes of 3D Scene**
Developers can scale only geometries of a 3D node or all nodes of 3D Scene. In order to achieve this, developers can call multiple Scale members of the PolygonModifier class instance. This is the code example to scale all nodes or single node:



**Python**

```py

from aspose.threed.utilities import Vector3
from aspose.threed.entities import PolygonModifier, Box
from aspose.threed import Scene

# scale the model in huge-scene.obj by 0.01 and save it to another file:

scene = Scene.from_file("huge-scene.obj")

# create a Box instance

box = scene.root_node.create_child_node("box", Box())

# scale geometries of a single node

PolygonModifier.scale(box, Vector3(0.01));

# scale geometries of all nodes

PolygonModifier.scale(scene, Vector3(0.01));

scene.save("scaled-scene.obj", FileFormat.WAVEFRONT_OBJ)

```
