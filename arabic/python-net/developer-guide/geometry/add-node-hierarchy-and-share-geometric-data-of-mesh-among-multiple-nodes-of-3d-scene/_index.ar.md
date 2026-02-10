---
title: أضف التسلسل الهرمي للعقدة وشارك البيانات الهندسية للشبكة بين العقد المتعددة لمشهد 3D
type: docs
weight: 40
url: /ar/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: يعرض Aspose.3D for Python via .NET إنشاء تسلسل هرمي للعقدة. العقدة هي كتلة البناء الأساسية للمشهد. يحدد التسلسل الهرمي للعقد الهيكل المنطقي للمشهد ، ويوفر محتوى مرئيًا عن طريق إرفاق أشكال التعديل ، والأضواء ، والكاميرات بالعقد.
---
##  **أضف التسلسل الهرمي للعقدة في مستند مشهد 3D**
يعرض Aspose.3D for Python via .NET إنشاء تسلسل هرمي للعقدة. العقدة هي كتلة البناء الأساسية للمشهد. يحدد التسلسل الهرمي للعقد الهيكل المنطقي للمشهد ، ويوفر محتوى مرئيًا عن طريق إرفاق أشكال التعديل ، والأضواء ، والكاميرات بالعقد.
###  **Sسين rapراب Example**
A نموذج المشهد التسلسل الهرمي يشبه:

! [Todo: image_ altttext](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

في Aspose.3D ، يمكن أن يكون لكل مثيل `Node` عقد أطفال متعددة ، في هذا المثال ، أنشأنا عقدة بها عقدتان مكعبتان ، وإذا قمنا بتدوير عقدة الجذر ، تتأثر جميع العقد التابعة أيضًا:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.utilities import Quaternion, Vector3
import math

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Get a child node object
top = scene.root_node.create_child_node()
#  Each cube node has their own translation
cube1 = top.create_child_node("cube1")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the mesh
cube1.entity = mesh
#  Set first cube translation
cube1.transform.translation = Vector3(-10, 0, 0)
cube2 = top.create_child_node("cube2")
#  Point node to the mesh
cube2.entity = mesh
#  Set second cube translation
cube2.transform.translation = Vector3(10, 0, 0)
#  The rotated top node will affect all child nodes
top.transform.rotation = Quaternion.from_euler_angle(math.pi, 4, 0)
#  The path to the documents directory.
output = "out"  + "NodeHierarchy.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Des hare esh sh's omeeometry ata ata بين oultiple oodes**
لتقليل ضروريات الذاكرة ، يمكن ربط مثيل واحد لفئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) بمثيلات مختلفة من فئة [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node). تصور أنك تحتاج إلى نظام حيث يبدو أن جميع مكعبات 3D لا يمكن تمييزها ، لكنك طلبت عددًا كبيرًا منها. يمكنك حفظ الذاكرة عن طريق صنع كائن شبكي واحد عندما يبدأ النظام. عند تلك النقطة ، في كل مرة تطلب فيها شكلاً آخر ، تصنع جسم عقدة آخر ، ثم تشير إلى تلك العقدة إلى شبكة واحدة. وهذا ما يسمى التثبيت. يسمح Aspose.3D for Python via .NET APIs بالقيام بالتثبيت.
###  **مثال على ذلك**
في ألعاب RTS (استراتيجية الوقت الفعلي) مثل ، يمكننا دائمًا رؤية أجهزة NPCs متعددة (شخصية غير لاعب) بنفس الطراز 3D ، ربما بألوان مختلفة ، مما يجعل المحرك عادةً يشارك بيانات هندسة الشبكة نفسها عبر أجهزة NPCs مختلفة ، وتسمى هذه التقنية التثبيت.

{{% alert color="primary" %}}

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة `Mesh` كما روى هناك](/3d/ar/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Emتوضيح رمز المثال:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.shading import LambertMaterial
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Define color vectors
colors = [Vector3(1, 0, 0), Vector3(0, 1, 0), Vector3(0, 0, 1)]
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
idx = 0
for color in colors:
    #  Initialize cube node object
    cube = Node("cube")
    cube.entity = mesh
    mat = LambertMaterial()
    #  Set color
    mat.diffuse_color = color
    #  Set material
    cube.material = mat
    #  Set translation
    cube.transform.translation = Vector3(idx * 20, 0, 0)
    idx = idx + 1
    #  Add cube node
    scene.root_node.child_nodes.append(cube)
#  The path to the documents directory.
output = "out"  + "MeshGeometryData.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7400ASCII)

{{< /highlight >}}

In هذا المثال أنشأنا 3 العقد مكعب حصة نفس الشبكة ، كل واحد منهم لديها مواد مختلفة بألوان مختلفة.
