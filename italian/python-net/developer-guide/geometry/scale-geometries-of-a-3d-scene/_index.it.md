---
title: Geometrie in scala di una scena 3D
type: docs
weight: 70
url: /it/python-net/scale-geometries-of-a-3d-scene/
description: Gli sviluppatori possono scalare solo le geometrie di un nodo 3D o tutti i nodi della scena 3D. Per raggiungere questo obiettivo, gli sviluppatori possono chiamare più membri Scale dell'istanza della classe PolygonModifier.
---
## **Geometrie di scala di un singolo nodo 3D o di tutti i nodi della scena 3D**
Gli sviluppatori possono scalare solo le geometrie di un nodo 3D o tutti i nodi della scena 3D. Per raggiungere questo obiettivo, gli sviluppatori possono chiamare più membri Scale dell'istanza della classe `PolygonModifier`. Questo è l'esempio di codice per scalare tutti i nodi o singolo nodo:



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
