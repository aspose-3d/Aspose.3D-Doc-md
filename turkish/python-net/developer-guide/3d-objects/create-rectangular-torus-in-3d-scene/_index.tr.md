---
title: 3D sahnesinde dikdörtgen torus oluştur
type: docs
weight: 50
url: /tr/python-net/create-rectangular-torus-in-3d-scene/
description: Using Aspose.3D for Python via .NET API, developers can create 3D objects, and then save 3D scene in any supported 3D format.
---
{{% alert color="primary" %}} 

Using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, developers can create 3D objects, and then save 3D scene in any supported 3D format.

{{% /alert %}} 
##  **Angular ectangular Torus**
We have added `RectangularTorus` class, it allows developers to place a parameterized rectangular torus into the scene, this can be converted to ordinal mesh/triangle mesh during saving the scene into different supported file formats.

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

To dikdörtgen torus aşağıdaki gibi görünüyor:

! [Todo: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
