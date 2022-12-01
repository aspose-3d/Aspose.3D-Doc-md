---
title: Создать прямоугольный Torus в 3D Сцена
type: docs
weight: 50
url: /ru/python-net/create-rectangular-torus-in-3d-scene/
description: Используя Aspose.3D для Python via .NET API, разработчики могут создавать объекты 3D, а затем сохранять сцену 3D в любом поддерживаемом формате 3D.
---
{{% alert color="primary" %}} 

Используя[Aspose.3D для Python via .NET](https://products.aspose.com/3d/python-net/)API разработчики могут создавать объекты 3D, а затем сохранять сцену 3D в любом поддерживаемом формате 3D.

{{% /alert %}} 
## **Прямоугольный тор**
Мы добавили класс `RectangularTorus`, он позволяет разработчикам помещать в сцену параметризованный прямоугольный тор, его можно преобразовать в порядковые сетки/треугольную сетку во время сохранения сцены в различные поддерживаемые форматы файлов.

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

![Todo: изображение_Альт_Текст](create-rectangular-torus-in-3d-scene_1.png)
