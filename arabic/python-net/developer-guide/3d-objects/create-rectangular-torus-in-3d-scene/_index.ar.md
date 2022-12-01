---
title: Create مستطيلة Torus في 3D cencene
type: docs
weight: 50
url: /ar/python-net/create-rectangular-torus-in-3d-scene/
description: Sing sing Aspose.3D ل Python via .NET API ، يمكن للمطورين إنشاء 3D الكائنات ، ومن ثم حفظ 3D المشهد في أي تنسيق معتمد 3D.
---
{{% alert color="primary" %}} 

Uالغناء[Aspose.3D ل Python via .NET](https://products.aspose.com/3d/python-net/)API ، يمكن للمطورين إنشاء أشياء 3D ، ثم حفظ 3D المشهد في أي تنسيق 3D المدعومة.

{{% /alert %}} 
## **Rالزاوية الأمامية orus**
Added e أضافت `RectangularTorus` الفئة ، فإنه يسمح للمطورين لوضع توروس مستطيلة متناظرة في المشهد ، وهذا يمكن تحويلها إلى شبكة/مثلث شبكة عادية أثناء حفظ المشهد في تنسيقات الملفات المدعومة المختلفة.

**Python**

```py

import math
from aspose.threed.entities import RectangularTorus

rt = RectangularTorus()

rt.inner_radius = 17

rt.outer_radius = 22

rt.height = 30

rt.arc = math.pi * 0.5

scene = Scene()

scene.root_node.create_child_node(rt)

scene.save("rtorus.obj", FileFormat.WAVEFRONT_OBJ)

```

Tانه ولد توروس مستطيلة تبدو على النحو التالي:

![تودو: الصورة_البديل_نص](create-rectangular-torus-in-3d-scene_1.png)
