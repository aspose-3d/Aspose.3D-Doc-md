---
title: Crear un toro rectangular en la escena 3D
type: docs
weight: 50
url: /es/python-net/create-rectangular-torus-in-3d-scene/
description: Usando Aspose.3D for Python via .NET API, los desarrolladores pueden crear objetos 3D y luego guardar la escena 3D en cualquier formato 3D compatible.
---
{{% alert color="primary" %}} 

Usando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, los desarrolladores pueden crear objetos 3D y luego guardar la escena 3D en cualquier formato 3D compatible.

{{% /alert %}} 
##  **Torus rectangular**
Hemos agregado la clase `RectangularTorus`, permite a los desarrolladores colocar un toro rectangular parametrizado en la escena, esto se puede convertir en malla ordinal/malla triangular durante el guardado de la escena en diferentes formatos de archivo compatibles.

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

El toro rectangular generado se ve de la siguiente manera:

¡! [Todo: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
