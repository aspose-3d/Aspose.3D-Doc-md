---
title: Quaternionen verkettieren und auf 3D Entitäten anwenden
type: docs
weight: 50
url: /de/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: Mit Aspose.3D for Python via .NET können Entwickler zwei Rotations transformationen zu einer in einer Quaternion dargestellten kombinieren.
---
{{% alert color="primary" %}} 

Mit [Aspose.3D for Python via .NET](https://www.aspose.com/products/3d) können Entwickler zwei Rotations transformationen zu einer in einer Quaternion dargestellten kombinieren.

{{% /alert %}} 
##  **Quaternionen verkettieren**
Quaternionen werden verwendet, um eine Orientierung im Raum 3D darzustellen. Die `concat`-Methode der [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion)-Klasse kann verwendet werden, um zwei Quaternionen zu kombinieren. In diesem Code beispiel kombinieren wir zwei Quaternionen und erhalten eine dritte resultierende Quaternion. Anschließend wenden wir diese drei Quaternionen auf drei Zylinder an.
###  **Programmier probe**
Dieses Code beispiel kombiniert zwei Quaternionen und wendet sie auf verschiedene Zylinder an.

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


**Ergebnis in 3ds MAX**

! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
