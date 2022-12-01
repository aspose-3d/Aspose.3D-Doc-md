---
title: Create dikdörtgen Torus 3D cene cene
type: docs
weight: 50
url: /tr/python-net/create-rectangular-torus-in-3d-scene/
description: Python via .NET API için sing sing Aspose.3D, geliştiriciler 3D nesnelerini oluşturabilir ve sonra 076. 481 formatındaki herhangi bir sahneyi kaydedebilir.
---
{{% alert color="primary" %}} 

Using[Python via .NET için Aspose.3D](https://products.aspose.com/3d/python-net/)API, geliştiriciler 3D nesnelerini oluşturabilir ve 3D sahnesini desteklenen herhangi bir 3D formatında kaydedebilir.

{{% /alert %}} 
## **Angular ectangular Torus**
We `RectangularTorus` sınıfı ekledi, geliştiricilerin sahne içine parametreli dikdörtgen bir torus yerleştirmelerine izin veriyor, bu, sahneyi farklı desteklenen dosya formatlarına kaydederken sıra dışı örgü/üçgen örgüye dönüştürülebilir.

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

![Todo: görüntü_Alt_Metin](create-rectangular-torus-in-3d-scene_1.png)
