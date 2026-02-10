---
title: 连接四元数并应用于 3D 实体
type: docs
weight: 50
url: /zh/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Python via .NET 允许开发人员将两个旋转转换合并为一个以四元数表示的转换。
---
{{% alert color="primary" %}} 

[Aspose.3D for Python via .NET](https://www.aspose.com/products/3d) 允许开发人员将两个旋转转换合并为一个以四元数表示的转换。

{{% /alert %}} 
##  **级联四元数**
四元数用于表示 3D 空间中的方向。由 [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) 类公开的 `concat` 方法可用于组合两个四元数。在此代码示例中，我们组合两个四元数并获得第三个结果四元数，然后将这三个四元数应用于三个圆柱体。
###  **编程示例**
此代码示例将两个四元数组合在一起，并将它们应用于不同的圆柱体。

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Cylinder
from aspose.threed.utilities import Quaternion, Vector3
import math

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
scene = Scene()
q1 = Quaternion.from_euler_angle(math.pi * 0.5, 0, 0)
q2 = Quaternion.from_angle_axis(-math.pi * 0.5, Vector3.X_AXIS)
#  Concatenate q1 and q2. q1 and q2 rotate alone x-axis with same angle but different direction,
#  So the concatenated result will be identity quaternion.
q3 = q1.concat(q2)
#  Create 3 cylinders to represent each quaternion
cylinder = scene.root_node.create_child_node("cylinder-q1", Cylinder(0.1, 1, 2))
cylinder.transform.rotation = q1
cylinder.transform.translation = Vector3(-5, 2, 0)
cylinder = scene.root_node.create_child_node("cylinder-q2", Cylinder(0.1, 1, 2))
cylinder.transform.rotation = q2
cylinder.transform.translation = Vector3(0, 2, 0)
cylinder = scene.root_node.create_child_node("cylinder-q3", Cylinder(0.1, 1, 2))
cylinder.transform.rotation = q3
cylinder.transform.translation = Vector3(5, 2, 0)
output = "out"  + "test_out.fbx"
#  Save to file
scene.save(output, FileFormat.FBX7400ASCII)

{{< /highlight >}}


**结果3ds MAX**

![todo: 图像 _ alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
