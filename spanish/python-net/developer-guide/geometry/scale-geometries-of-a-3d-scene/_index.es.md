---
title: Geometrías de escala de una escena 3D
type: docs
weight: 70
url: /es/python-net/scale-geometries-of-a-3d-scene/
description: Los desarrolladores pueden escalar solo las geometrías de un nodo 3D o todos los nodos de 3D Scene. Para lograr esto, los desarrolladores pueden llamar a varios miembros de Scale de la instancia de la clase PolygonModifier.
---
##  **Geometrías de escala de un solo nodo 3D o de todos los nodos de la escena 3D**
Los desarrolladores pueden escalar solo las geometrías de un nodo 3D o todos los nodos de 3D Scene. Para lograr esto, los desarrolladores pueden llamar a varios miembros de Scale de la instancia de la clase `PolygonModifier`. Este es el ejemplo de código para escalar todos los nodos o un solo nodo:



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
