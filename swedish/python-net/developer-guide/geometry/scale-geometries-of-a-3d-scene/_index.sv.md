---
title: Skala geometrier för en 3D Scene
type: docs
weight: 70
url: /sv/python-net/scale-geometries-of-a-3d-scene/
description: Utvecklare kan endast skala geometrier av en 3D nod eller alla noder av 3D Scene. För att uppnå detta, kan utvecklare ringa flera Scale medlemmar av PolygonModifier klass instans.
---
## **Skala geometrier av en enda 3D nod eller alla noder av 3D Scene**
Utvecklare kan endast skala geometrier av en 3D nod eller alla noder av 3D Scene. För att uppnå detta kan utvecklare kalla flera Scale medlemmar av klassen `PolygonModifier` instans. Detta är kodexemplet för att skala alla noder eller enstaka nod:



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
