---
title: 与气缸一起工作
type: docs
weight: 130
url: /zh/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET 允许自定义圆柱体的偏移顶部。为了使用此功能，可以使用Cylinder类的Offset属性。
---
#  **自定义偏移顶部**
Aspose.3D for Python via .NET 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用 `Cylinder` 类的 `offset` 属性。以下代码段显示了如何自定义偏移顶部:



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

![todo: 图像 _ alt_text](working-with-cylinder_1.png)

左边的 `offset_top` 设置为 (5，3，0)，很容易看到顶帽已经移动，整个躯干也受到影响。
#  **自定义剪切底部**
Aspose.3D for Python via .NET 允许自定义圆柱体的剪切底部。为了使用此功能，您可以使用 `Cylinder` 类的 `shear_bottom` 属性。以下代码段显示了如何自定义剪切底部:



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

![todo: 图像 _ alt_text](working-with-cylinder_2.png)

左侧圆柱体有 `shear_bottom` 到 (0，0.83)，而右侧圆柱体是一个有序圆柱体。
#  **创建风扇气缸**
Aspose.3D for Python via .NET 允许创建一个风扇圆柱体。为了使用此功能，您可以将 `Cylinder` 类的 `generate_fan_cylinder` 属性设置为 `True`。以下代码段显示了如何使用此功能:



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

![todo: 图像 _ alt_text](working-with-cylinder_3.png)

左侧气缸有 `generate_fan_cylinder = False`，右侧气缸有 `generate_fan_cylinder = True`。
