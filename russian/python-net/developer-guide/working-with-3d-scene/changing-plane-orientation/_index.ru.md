---
title: Изменение ориентации плоскости
type: docs
weight: 40
url: /ru/python-net/changing-plane-orientation/
description: Aspose.3D for Python via .NET позволяет изменять ориентацию сцены. Для того чтобы изменить ориентацию, в классе плоскости вводится свойство вектора вверх.
---
#  **Изменение ориентации плоскости**
Aspose.3D for Python via .NET позволяет изменять ориентацию сцены. Чтобы изменить ориентацию, в класс `Plane` вводится свойство `up` vector. Следующий фрагмент кода показывает, как изменить ориентацию самолета:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Plane
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the data directory
dataDir = "data-dir"
#  Initialize scene object
scene = Scene()
plane = Plane()
plane.up = Vector3(1, 1, 3)
#  Set Vector
scene.root_node.create_child_node(plane)
# This will generate a plane that has customized orientation
scene.save(dataDir + "ChangePlaneOrientation.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
