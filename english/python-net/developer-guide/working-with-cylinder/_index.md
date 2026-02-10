---
title: Working with Cylinder
type: docs
weight: 130
url: /python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET allows customizing Offset Top of a cylinder. In order to use this functionality, you can use Offset property of Cylinder class.
---

# **Customize Offset Top**
Aspose.3D for Python via .NET allows customizing Offset Top of a cylinder. In order to use this functionality, you can use `offset` property of `Cylinder` class. The following code snippet shows how to customize Offset Top:



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

![todo:image_alt_text](working-with-cylinder_1.png)

The left one has `offset_top` set to (5, 3, 0), it's easy to see the top cap has moved and the whole torso also gets affected.
# **Customize ShearBottom**
Aspose.3D for Python via .NET allows customizing shear bottom of a cylinder. In order to use this functionality, you can use `shear_bottom` property of `Cylinder` class. The following code snippet shows how to customize Shear Bottom:


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
#  Add cylinder 1 to scene
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Create cylinder 2
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Add cylinder to without a ShearBottom to the scene
scene.root_node.create_child_node(cylinder2)
#  Save scene
scene.save("data-dir"  + "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONT_OBJ)
{{< /highlight >}}

![todo:image_alt_text](working-with-cylinder_2.png)

The left cylinder has `shear_bottom` to (0, 0.83) while the right one is an ordinal cylinder.
# **Create Fan-Cylinder**
Aspose.3D for Python via .NET allows creating a fan cylinder. In order to use this functionality, you can set `generate_fan_cylinder` property of `Cylinder` class to `True`. The following code snippet shows how to use this functionality:


{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import MathUtils, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Create a cylinder
fan = Cylinder(2, 2, 10, 20, 1, False)
#  Set GenerateGanCylinder to true
fan.generate_fan_cylinder = True
#  Set ThetaLength
fan.theta_length = MathUtils.to_radian(270)
#  Create ChildNode
scene.root_node.create_child_node(fan).transform.translation = Vector3(10, 0, 0)
#  Create a cylinder without a fan
nonfan = Cylinder(2, 2, 10, 20, 1, False)
#  Set GenerateGanCylinder to false
nonfan.generate_fan_cylinder = False
#  Set ThetaLengeth
nonfan.theta_length = MathUtils.to_radian(270)
#  Create ChildNode
scene.root_node.create_child_node(nonfan)
#  Save scene
scene.save("data-dir"  + "CreateFanCylinder.obj", FileFormat.WAVEFRONT_OBJ)
{{< /highlight >}}

![todo:image_alt_text](working-with-cylinder_3.png)

The left cylinder has `generate_fan_cylinder = False` and the right one has `generate_fan_cylinder = True`.
