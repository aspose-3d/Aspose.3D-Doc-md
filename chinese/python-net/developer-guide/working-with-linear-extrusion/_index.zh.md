---
title: 与线性挤压一起工作
type: docs
weight: 110
url: /zh/python-net/working-with-linear-extrusion/
description: Aspose.3D for Python via .NET 提供了linearexdution类，它将2D形状作为输入，并在第三维中扩展该形状。
---
#  **进行线性挤压**
Aspose.3D for Python via .NET 提供 `LinearExtrusion` 类，它将2D形状作为输入，并在第三维中扩展该形状。以下代码段显示了如何执行线性挤出:



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
#  **线性挤压中的 “切片”**
Aspose.3D for Python via .NET 提供 `LinearExtrusion` 类的 `slices` 属性。`slices` 属性定义沿挤出路径的中间点的数量。以下代码段显示了如何在线性挤出中使用 `slices` 属性:



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
#  **线性挤压中的 “中心”**
Aspose.3D for Python via .NET 提供 `LinearExtrusion` 类的 `center` 属性。如果 `center` 属性设置为 `True`，则挤出范围是从-Height/2到Height/2，否则，挤出是从0到Height。以下代码段显示了如何在线性挤出中使用 `center` 属性:



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
#  **线性挤压中的 “扭曲”**
Aspose.3D for Python via .NET 提供 `LinearExtrusion` 类的 `twist` 属性。`twist` 属性处理挤出形状时的旋转程度。以下代码段显示了如何在线性挤出中使用 `twist` 属性:



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
#  **线性挤压中的 “扭曲 _ 偏移”**
Aspose.3D for Python via .NET 提供 `LinearExtrusion` 类的 `twist_offset` 属性。`twist_offset` 属性在旋转挤出时平移偏移。以下代码段显示了如何在线性挤出中使用 `twist_offset` 属性:



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
#  **线性挤压中的 “方向”**
Aspose.3D for Python via .NET 提供 `LinearExtrusion` 类的 `direction` 属性。`direction` 属性定义挤出的方向。以下代码段显示了如何在线性挤出中使用 `direction` 属性:



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
