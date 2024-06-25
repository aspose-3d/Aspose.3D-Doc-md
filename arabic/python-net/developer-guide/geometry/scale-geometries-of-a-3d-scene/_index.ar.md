---
title: أشكال هندسية بمقياس لمشهد 3D
type: docs
weight: 70
url: /ar/python-net/scale-geometries-of-a-3d-scene/
description: يمكن للمطورين قياس الأشكال الهندسي فقط بعقدة 3D أو جميع عُقد مشهد 3D. من أجل تحقيق ذلك ، يمكن للمطورين استدعاء أعضاء نطاق متعددة من مثيل فئة PolygonModifier.
---
##  **أشكال أشكال أشكال حجم عقدة واحدة 3D أو جميع عُقد مشهد 3D**
يمكن للمطورين قياس الأشكال الهندسي فقط بعقدة 3D أو جميع عُقد مشهد 3D. من أجل تحقيق ذلك ، يمكن للمطورين استدعاء عدة أعضاء مقياس في مثيل فئة `PolygonModifier`. هذا هو مثال رمز لتوسيع نطاق جميع العقد أو عقدة واحدة:



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
