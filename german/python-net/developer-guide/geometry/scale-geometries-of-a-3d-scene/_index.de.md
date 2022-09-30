---
title: Maßstab Geometrien einer 3D Szene
type: docs
weight: 70
url: /de/python-net/scale-geometries-of-a-3d-scene/
description: Entwickler können nur Geometrien eines Knotens 3D oder aller Knoten der Szene 3D skalieren. Um dies zu erreichen, können Entwickler mehrere Scale-Mitglieder der PolygonModifier-Klassen instanz aufrufen.
---
## **Skalierung geometrien eines einzelnen Knotens 3D oder aller Knoten der Szene 3D**
Entwickler können nur Geometrien eines Knotens 3D oder aller Knoten der Szene 3D skalieren. Um dies zu erreichen, können Entwickler mehrere Scale-Mitglieder der Klassen instanz `PolygonModifier` aufrufen. Dies ist das Code beispiel, um alle Knoten oder einzelnen Knoten zu skalieren:



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
