---
title: Cylinder ile king orking
type: docs
weight: 130
url: /tr/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET, bir silindirin ofset üstünü özelleştirmeye izin verir. Bu işlevselliği kullanmak için silindir sınıfının ofset özelliğini kullanabilirsiniz.
---
#  **Oustomize ffffset Top**
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

! [Todo: image_alt_text](working-with-cylinder_1.png)

The left one has `offset_top` set to (5, 3, 0), it's easy to see the top cap has moved and the whole torso also gets affected.
#  **Customize hearhearhearottom**
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
#  Add cylinder 1 to the scene
scene.root_node.create_child_node(cylinder1).transform.translation = Vector3(10, 0, 0)
#  Create cylinder 2
cylinder2 = Cylinder(2, 2, 10, 20, 1, False)
#  Add cylinder to without a ShearBottom to the scene
scene.root_node.create_child_node(cylinder2)
#  Save scene
scene.save("data-dir"  + "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

The left cylinder has `shear_bottom` to (0, 0.83) while the right one is an ordinal cylinder.
#  **Create Fan-Cylinder**
Aspose.3D for Python via .NET allows creating a fan cylinder. In order to use this functionality, you can set `generate_fan_cylinder` property of `Cylinder` class to `True`. The following code snippet shows how to use this functionality:



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

! [Todo: image_alt_text](working-with-cylinder_3.png)

The left cylinder has `generate_fan_cylinder = False` and the right one has `generate_fan_cylinder = True`.
