---
title: Работа с цилиндром
type: docs
weight: 130
url: /ru/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET позволяет настроить Offset Top цилиндра. Для того, чтобы использовать эту функциональность, вы можете использовать свойство Offset класса Cylinder.
---
#  **Настроить офсетный топ**
Aspose.3D for Python via .NET позволяет настроить Offset Top цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `offset` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a scene
scene = Scene()
#  Initialize cylinder
cylinder1 = Cylinder(2, 2, 10, 20, 1, False)
#  Set OffsetTop
cylinder1.offset_top = Vector3(5, 3, 0)
#  Create ChildNode
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Intialze second cylinder without customized OffsetTop
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Create ChildNode
scene.root_node.create_child_node(cylinder2)
#  Save
scene.save("data-dir" + "CustomizedOffsetTopCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

! [Для: имаге_альт_текст](working-with-cylinder_1.png)

На левой стороне `offset_top` установлено значение (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и все туловище также пострадало.
#  **Настроить ShearBottom**
Aspose.3D for Python via .NET позволяет настраивать срезное дно цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `shear_bottom` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить дно сдвига:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Vector2, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a scene
scene = Scene()
#  Create cylinder 1
cylinder1 = Cylinder(2, 2, 10, 20, 1, False)
#  Customized shear bottom for cylinder 1
cylinder1.shear_bottom = Vector2(0, 0.83)
#  Add cylinder 1 to the scene
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Create cylinder 2
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Add cylinder to without a ShearBottom to the scene
scene.root_node.create_child_node(cylinder2)
#  Save scene
scene.save("data-dir"  + "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

! [Для: имаге_альт_текст](working-with-cylinder_2.png)

Левый цилиндр имеет от `shear_bottom` до (0, 0,83), а правый-порядковый цилиндр.
#  **Создать вентилятор-цилиндр**
Aspose.3D for Python via .NET позволяет создать цилиндр вентилятора. Чтобы использовать эту функцию, вы можете установить свойство `generate_fan_cylinder` класса `Cylinder` на `True`. Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Vector2, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a scene
scene = Scene()
#  Create cylinder 1
cylinder1 = Cylinder(2, 2, 10, 20, 1, False)
#  Customized shear bottom for cylinder 1
cylinder1.shear_bottom = Vector2(0, 0.83)
#  Add cylinder 1 to the scene
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Create cylinder 2
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Add cylinder to without a ShearBottom to the scene
scene.root_node.create_child_node(cylinder2)
#  Save scene
scene.save("data-dir"  + "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

! [Для: имаге_альт_текст](working-with-cylinder_3.png)

Левый цилиндр имеет `generate_fan_cylinder = False`, а правый-`generate_fan_cylinder = True`.
