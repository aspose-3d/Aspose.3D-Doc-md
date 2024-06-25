---
title: Skapa rektangulärt torus i 3D Scene
type: docs
weight: 50
url: /sv/python-net/create-rectangular-torus-in-3d-scene/
description: Genom att använda Aspose.3D for Python via .NET API, kan utvecklare skapa 3D objekt, och sedan spara 3D scen i vilket 3D-format som stöds.
---
{{% alert color="primary" %}} 

Genom att använda [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, kan utvecklare skapa 3D objekt, och sedan spara 3D scen i vilket 3D-format som stöds.

{{% /alert %}} 
##  **Rektangulär torus**
Vi har lagt till `RectangularTorus` klass, det tillåter utvecklare att placera en parameteriserad rektangulär torus i scenen, Detta kan konverteras till ordinarie mesh/triangelt mesh under att spara scenen till olika filformat som stöds.

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

Den genererade rektangulära torus ser ut enligt följande:

![todo:image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
