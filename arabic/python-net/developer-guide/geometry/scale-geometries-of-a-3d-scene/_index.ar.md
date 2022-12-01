---
title: Scale هندسي من 3D cencene
type: docs
weight: 70
url: /ar/python-net/scale-geometries-of-a-3d-scene/
description: Dإيفلين يمكن أن مقياس هندسي فقط من عقدة 3D أو جميع العقد من 3D cenسين. In من أجل تحقيق ذلك ، يمكن للمطورين استدعاء أعضاء cale متعددة من فئة olyأوليغونوديفير سبيل المثال.
---
## **Scale هندسي عقدة واحدة 3D أو جميع العقد من 3D Scene**
Dإيفلين يمكن أن مقياس هندسي فقط من عقدة 3D أو جميع العقد من 3D cenسين. In من أجل تحقيق ذلك ، يمكن للمطورين استدعاء أعضاء cale متعددة من الدرجة `PolygonModifier` سبيل المثال. Tله هو مثال رمز لقياس جميع العقد أو عقدة واحدة:



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
