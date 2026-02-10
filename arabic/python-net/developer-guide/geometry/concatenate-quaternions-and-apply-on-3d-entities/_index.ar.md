---
title: رباعيات متسلسلة وتقدم الطلب على كيانات 3D
type: docs
weight: 50
url: /ar/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: يسمح Aspose.3D for Python via .NET للمطورين بدمج تحولي دوران إلى تحويل واحد ممثل في رباعي.
---
{{% alert color="primary" %}} 

يسمح [Aspose.3D for Python via .NET](https://www.aspose.com/products/3d) للمطورين بدمج تحولي دوران إلى تحويل واحد ممثل في رباعي.

{{% /alert %}} 
##  **Concatenate uuaternions**
تُستخدم كواتيرنيون لتمثيل اتجاه في مساحة 3D. يمكن استخدام طريقة `concat` المعروضة بواسطة فئة [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) للجمع بين رباعي. في هذا المثال البرمجي ، ندمج اثنين من رباعي الأيونات ونحصل على رباعي ثالث ناتج ، ثم نطبق هذه الرباعي الثلاثة على ثلاث أسطوانات.
###  **Pروغرامينغ ple وافرة**
Tله رمز المثال الجمع بين اثنين من رباتيرفيونس وتطبيقها على اسطوانات مختلفة.

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


**Result في 3ds MAX**

! [Todo: image_ altttext](concatenate-quaternions-and-apply-on-3d-entities_1.png)
