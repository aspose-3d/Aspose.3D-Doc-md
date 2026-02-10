---
title: Concaténer les quaternions et appliquer sur les entités 3D
type: docs
weight: 50
url: /fr/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Python via .NET permet aux développeurs de combiner deux transformation de rotation en une seule représentée dans un quaternion.
---
{{% alert color="primary" %}} 

[Aspose.3D for Python via .NET](https://www.aspose.com/products/3d) permet aux développeurs de combiner deux transformation de rotation en une seule représentée dans un quaternion.

{{% /alert %}} 
##  **Quaternions concaténer**
Les quaternions sont utilisés pour représenter une orientation dans l'espace 3D. La méthode `concat` exposée par la classe [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) peut être utilisée pour combiner deux quaternions. Dans cet exemple de code, nous combinons deux quaternions et obtenons un troisième quaternion résultant, puis nous appliquons ces trois quaternions à trois cylindres.
###  **Échantillon de programmation**
Cet exemple de code combine deux quaternions et les applique à différents cylindres.

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


**Résultat dans 3ds MAX**

! [Tout le monde: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
