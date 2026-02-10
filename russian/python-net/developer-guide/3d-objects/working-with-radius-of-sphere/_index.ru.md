---
title: Работа с радиусом сферы
type: docs
weight: 110
url: /ru/python-net/working-with-radius-of-sphere/
description: Используя Aspose.3D for Python via .NET, вы можете установить радиус получения сферы. Для того чтобы получить или задать радиус, вы можете использовать свойство Radius класса Sphere. Ниже приведен пример кода для установки радиуса сферы.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,4 или выше.

{{% /alert %}} 
##  **Работа с радиусом сферы**
Используя Aspose.3D for Python via .NET, вы можете установить радиус получения сферы. Чтобы получить или задать радиус, вы можете использовать свойство `radius` класса `Sphere`. Ниже приведен пример кода для установки радиуса сферы.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
sphere = Sphere()
sphere.radius = 10 .0
#  Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.root_node.create_child_node(sphere)
#  Save scene
scene.save("data-dir"  + "sphere.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
