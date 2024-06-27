---
title: 缩放 3D 场景的几何图形
type: docs
weight: 70
url: /zh/python-net/scale-geometries-of-a-3d-scene/
description: 开发人员只能缩放 3D 节点或 3D 场景的所有节点的几何图形。为了实现这一点，开发人员可以调用PolygonModifier类实例的多个Scale成员。
---
##  **缩放单个 3D 节点或 3D 场景的所有节点的几何图形**
开发人员只能缩放 3D 节点或 3D 场景的所有节点的几何图形。为了实现这一点，开发人员可以调用 `PolygonModifier` 类实例的多个Scale成员。这是缩放所有节点或单个节点的代码示例:



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
