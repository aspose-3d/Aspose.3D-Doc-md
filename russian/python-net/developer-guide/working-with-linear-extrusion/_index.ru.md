---
title: Работа с линейной экструзионной
type: docs
weight: 110
url: /ru/python-net/working-with-linear-extrusion/
description: Aspose.3D for Python via .NET предлагает класс LinearExtrusion, который принимает 2D форму в качестве входных данных и расширяет форму в 3-м измерении.
---
#  **Выполнение линейной экструзии**
Aspose.3D for Python via .NET предлагает класс `LinearExtrusion`, который принимает 2D форму в качестве входных данных и расширяет форму в 3-м измерении. Следующий фрагмент кода показывает, как выполнить линейную экструзию:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
extrusion = LinearExtrusion(profile, 10)
extrusion.slices = 100
extrusion.center = True
extrusion.twist = 360.0
extrusion.twist_offset = Vector3(10, 0, 0)
#  Perform Linear extrusion by passing a 2D profile as input and extend the shape in the 3rd dimension
extrusion = extrusion
#  Create a scene
scene = Scene()
#  Create a child node by passing extrusion
scene.root_node.create_child_node(extrusion)
#  Save 3D scene
scene.save("out"  + "LinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Нарез' в линейной экструзии**
Aspose.3D for Python via .NET предлагает свойство `slices` класса `LinearExtrusion`. Свойство `slices` определяет количество промежуточных точек вдоль пути выдавливания. Следующий фрагмент кода показывает, как использовать свойство `slices` в линейной экструзии:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(15, 0, 0)
extrusion = LinearExtrusion(profile, 2)
extrusion.slices = 2 
#  Slices parameter defines the number of intermediate points along the path of the extrusion
#  Perform linear extrusion on left node using slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 2)
extrusion2.slices = 10 
#  Perform linear extrusion on right node using slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "SlicesInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **«Центр» в линейной экструзии**
Aspose.3D for Python via .NET предлагает свойство `center` класса `LinearExtrusion`. Если для свойства `center` установлено значение `True`, диапазон выдавливания будет от-Height/2 до Height/2, в противном случае выдавливание будет от 0 до Height. Следующий фрагмент кода показывает, как использовать свойство `center` в линейной экструзии:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(15, 0, 0)
extrusion = LinearExtrusion(profile, 2)
extrusion.slices = 2 
#  Slices parameter defines the number of intermediate points along the path of the extrusion
#  Perform linear extrusion on left node using slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 2)
extrusion2.slices = 10 
#  Perform linear extrusion on right node using slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "SlicesInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Твист' в линейной экструзии**
Aspose.3D for Python via .NET предлагает свойство `twist` класса `LinearExtrusion`. `twist` свойство обрабатывает степень вращения при выдавливании формы. Следующий фрагмент кода показывает, как использовать свойство `twist` в линейной экструзии:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create rifht node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(15, 0, 0)
extrusion = LinearExtrusion(profile, 10)
extrusion.twist = 0.0
extrusion.slices = 100 
#  Twist property defines the degree of the rotation while extruding the profile
#  Perform linear extrusion on left node using twist and slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 10)
extrusion2.twist = 90.0
extrusion2.slices = 100 
#  Perform linear extrusion on right node using twist and slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "TwistInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Twist _ ofset' в линейной экструзии**
Aspose.3D for Python via .NET предлагает свойство `twist_offset` класса `LinearExtrusion`. `twist_offset` свойство переводит смещение при вращении выдавливания. Следующий фрагмент кода показывает, как использовать свойство `twist_offset` в линейной экструзии:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(18, 0, 0)
extrusion = LinearExtrusion(profile, 10)
extrusion.twist = 360.0
extrusion.slices = 100 
#  TwistOffset property is the translate offset while rotating the extrusion.
#  Perform linear extrusion on left node using twist and slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 10)
extrusion2.twist = 360.0
extrusion2.slices = 100
extrusion2.twist_offset = Vector3(3, 0, 0)
#  Perform linear extrusion on right node using twist, twist offset and slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "TwistOffsetInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **«Направление» в линейной экструзии**
Aspose.3D for Python via .NET предлагает свойство `direction` класса `LinearExtrusion`. Свойство `direction` определяет направление выдавливания. Следующий фрагмент кода показывает, как использовать свойство `direction` в линейной экструзии:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(8, 0, 0)
extrusion = LinearExtrusion(profile, 10)
extrusion.twist = 360.0
extrusion.slices = 100 
#  Direction property defines the direction of the extrusion.
#  Perform linear extrusion on left node using twist and slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 10)
extrusion2.twist = 360.0
extrusion2.slices = 100
extrusion2.direction = Vector3(0.3, 0.2, 1)
#  Perform linear extrusion on right node using twist, slices, and direction property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "DirectionInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
