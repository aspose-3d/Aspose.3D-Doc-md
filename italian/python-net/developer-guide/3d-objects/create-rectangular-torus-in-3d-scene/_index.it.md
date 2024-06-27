---
title: Crea Torus rettangolare in 3D scena
type: docs
weight: 50
url: /it/python-net/create-rectangular-torus-in-3d-scene/
description: Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono creare oggetti 3D e quindi salvare 3D in qualsiasi formato 3D supportato.
---
{{% alert color="primary" %}} 

Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, gli sviluppatori possono creare oggetti 3D e quindi salvare 3D in qualsiasi formato 3D supportato.

{{% /alert %}} 
##  **Torus rettangolare**
Abbiamo aggiunto una classe `RectangularTorus`, consente agli sviluppatori di inserire un toro rettangolare parametrizzato nella scena, questo può essere convertito in mesh/mesh triangolare ordinale durante il salvataggio della scena in diversi formati di file supportati.

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

Il toro rettangolare generato ha il seguente aspetto:

! [Todo: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
