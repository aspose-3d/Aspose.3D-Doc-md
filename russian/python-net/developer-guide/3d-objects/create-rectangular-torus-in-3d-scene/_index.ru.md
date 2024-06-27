---
title: Создайте прямоугольного тора в сцене 3D
type: docs
weight: 50
url: /ru/python-net/create-rectangular-torus-in-3d-scene/
description: Используя Aspose.3D for Python via .NET API, разработчики могут создавать объекты 3D, а затем сохранять сцену 3D в любом поддерживаемом формате 3D.
---
{{% alert color="primary" %}} 

Используя [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, разработчики могут создавать объекты 3D, а затем сохранять сцену 3D в любом поддерживаемом формате 3D.

{{% /alert %}} 
##  **Прямоугольный тор**
Мы добавили класс `RectangularTorus`, он позволяет разработчикам поместить в сцену параметризованный прямоугольный тор, который может быть преобразован в порядковый сетчатый/треугольный сетчатый во время сохранения сцены в различные поддерживаемые форматы файлов.

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

Сгенерированный прямоугольный тор выглядит следующим образом:

! [Для: имаге_альт_текст](create-rectangular-torus-in-3d-scene_1.png)
