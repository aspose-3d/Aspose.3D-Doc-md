---
title: Aدينغ رانسفورميشن إلى oode
type: docs
weight: 30
url: /ar/python-net/adding-transformation-to-the-node/
description: تُستخدم TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، قدمنا تحويل فئة للوصول إليها بـ Aspose.3D.
---
{{% alert color="primary" %}}

يعرض Aspose.3D for Python via .NET تدوير الكائنات في مساحة 3D. هناك ثلاث طرق لتحديد دوران الكائن في مساحة 3D وزوايا Euler و Quaternion والمصفوفة المخصصة ، وكلها مدعومة بفئة [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

تُستخدم TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، وقدمنا فئة `Transform` للوصول إليها بـ Aspose.3D. وتشمل التحولات في التخلف:

- تصنيف:
- Calالترسبات
- Rأوتيشن
- Hear سماع رسم الخرائط
- رسم الخرائط

{{% alert color="primary" %}}

كائن الفئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة `Mesh` كما روى هناك](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Rotate بواسطة Quaternion**
{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.utilities import Quaternion, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Set rotation
cubeNode.transform.rotation = Quaternion.from_rotation(Vector3(0, 1, 0), Vector3(0.3, 0.5, 0.1))
#  Set translation
cubeNode.transform.translation = Vector3(0, 0, 20)
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "TransformationToNode.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Rotate بواسطة Euler ngngles**
{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Euler angles
cubeNode.transform.euler_angles = Vector3(0.3, 0.1, -0.5)
#  Set translation
cubeNode.transform.translation = Vector3(0, 0, 20)
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "TransformationToNode.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Custom ranransformation atatrix**
We يمكن أيضا استخدام Matrix مباشرة:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.utilities import Matrix4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Set custom translation matrix
cubeNode.transform.transform_matrix = Matrix4(1, -0.3, 0, 0, 0.4, 1, 0.3, 0, 0, 0, 1, 0, 0, 20, 0, 1
)
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "TransformationToNode.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
