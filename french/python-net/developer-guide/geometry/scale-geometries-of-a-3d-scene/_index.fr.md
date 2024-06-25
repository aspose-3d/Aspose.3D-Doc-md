---
title: Géométries d'échelle d'une scène 3D
type: docs
weight: 70
url: /fr/python-net/scale-geometries-of-a-3d-scene/
description: Les développeurs ne peuvent mettre à l'échelle que les géométries d'un nœud 3D ou de tous les nœuds de la scène 3D. Pour ce faire, les développeurs peuvent appeler plusieurs membres Scale de l'instance de classe PolygonModifier.
---
##  **Géométries d'échelle d'un seul nœud 3D ou de tous les nœuds de la scène 3D**
Les développeurs ne peuvent mettre à l'échelle que les géométries d'un nœud 3D ou de tous les nœuds de la scène 3D. Pour ce faire, les développeurs peuvent appeler plusieurs membres Scale de l'instance de la classe `PolygonModifier`. Voici l'exemple de code pour mettre à l'échelle tous les nœuds ou un seul nœud:



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
