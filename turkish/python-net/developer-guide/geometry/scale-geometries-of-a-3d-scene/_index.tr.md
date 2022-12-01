---
title: Scale geometrileri 3D cene cene
type: docs
weight: 70
url: /tr/python-net/scale-geometries-of-a-3d-scene/
description: Developers sadece 3D düğümünün veya 3D cene cene tüm düğümlerinin geometrilerini ölçebilir. In bunu başarmak için, geliştiriciler olyolygongonodifier sınıf örneğinin birden fazla Scale üyesini arayabilir.
---
## **Tek bir 3D düğümünün veya 3D Scene tüm düğümlerinin Scale geometrileri**
Developers sadece 3D düğümünün veya 3D cene cene tüm düğümlerinin geometrilerini ölçebilir. In bunu başarmak için, geliştiriciler `PolygonModifier` sınıf örneğinin birden fazla Scale üyesini arayabilir. This, tüm düğümleri veya tek düğümleri ölçeklendirmek için kod örneğidir:



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
