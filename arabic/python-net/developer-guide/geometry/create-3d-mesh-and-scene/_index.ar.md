---
title: إنشاء 3D شبكة ومشهد
type: docs
weight: 10
url: /ar/python-net/create-3d-mesh-and-scene/
description: يتم تعريف A esh sh من خلال مجموعة من نقاط التحكم والعديد من المضلعات على الوجهين n حسب الحاجة. Tمقالته يوضح كيفية تعريف esh sh.
---
##  **إنشاء شبكة مكعبة 3D**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) is defined by a set of control points and the many n-sided polygons as needed. This article explains how to define a Mesh.

In الطلب على إنشاء سطح esh esh ، ونحن بحاجة إلى تحديد نقاط التحكم والمضلعات على النحو التالي:

- [Define Cأونتول oin](/3d/ar/python-net/create-3d-mesh-and-scene/)
- [إنشاء مضلعات بفئة PolygonBuilder](/3d/ar/python-net/create-3d-mesh-and-scene/)
- [Olyreate olyأوليغونز](/3d/ar/python-net/create-3d-mesh-and-scene/)

Here مثال على إرفاق مادة هونغ Pإلى عقدة مكعب:
###  **Define Cأونتول oin**
يتكون شبكة A من قبل مجموعة من نقاط التحكم في الفضاء ، والمضلعات لوصف سطح الشبكة ، لإنشاء شبكة ، ونحن بحاجة إلى تحديد نقاط التحكم:

{{% alert color="primary" %}}

نقاط التحكم لجميع أشكال الأعمال ذات الشكل بـ Aspose.3D تستخدم إحداثيًا متجانسًا ، لذا يكون `Vector4` بدلاً من `Vector3` في رمز المثال.

{{% /alert %}}

**Example:**

{{< highlight "python" >}}
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize control points
controlPoints = [Vector4(-5.0, 0.0, 5.0, 1.0), Vector4(5.0, 0.0, 5.0, 1.0), Vector4(5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 0.0, -5.0, 1.0), Vector4(5.0, 0.0, -5.0, 1.0), Vector4(5.0, 10.0, -5.0, 1.0), Vector4(-5.0, 10.0, -5.0, 1.0)]

{{< /highlight >}}


###  **Olyreate olyأوليغونز**
Tانه نقاط التحكم ليست قابلة للتأجير ، لجعل مكعب مرئية ، ونحن بحاجة إلى تحديد المضلعات في كل جانب:

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
controlPoints = DefineControlPoints()
#  Initialize mesh object
mesh = Mesh()
#  Add control points to the mesh
mesh.control_points.extend(controlPoints)
#  Create polygons to mesh
#  Front face (Z+)
mesh.create_polygon([0, 1, 2, 3 ])
#  Right side (X+)
mesh.create_polygon([1, 5, 6, 2 ])
#  Back face (Z-)
mesh.create_polygon([5, 4, 7, 6 ])
#  Left side (X-)
mesh.create_polygon([4, 0, 3, 7 ])
#  Bottom face (Y-)
mesh.create_polygon([0, 4, 5, 1 ])
#  Top face (Y+)
mesh.create_polygon([3, 2, 6, 7 ])

{{< /highlight >}}


###  **إنشاء مضلعات بفئة PolygonBuilder**
يمكننا أيضًا تحديد المضلع بواسطة الرؤوس بفئة `PolygonBuilder`:

{{< highlight "python" >}}
from aspose.threed.entities import Mesh, PolygonBuilder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
controlPoints = DefineControlPoints()
#  Initialize mesh object
mesh = Mesh()
#  Add control points to the mesh
mesh.control_points.extend(controlPoints)
#  Indices of the vertices per each polygon
indices = [    0, 1, 2, 3,     1, 5, 6, 2,     5, 4, 7, 6,     4, 0, 3, 7,     0, 4, 5, 1,     3, 2, 6, 7 // Top face (Y+)
]
vertexId = 0
builder = PolygonBuilder(mesh)
for face in range(6):
    #  Start defining a new polygon
    builder.begin()
    for v in range(4):
        #  The indice of vertice per each polygon
        builder.add_vertex(indices[vertexId])
        vertexId = vertexId + 1
    #  Finished one polygon
    builder.end()

{{< /highlight >}}

Now انها الانتهاء ، لجعل شبكة مرئية ، ونحن بحاجة إلى إعداد عقدة لذلك.
##  **How إلى ririesh**
شبكة ريانغتوليت غير مفيدة لصناعة اللعبة لأن الثلاثي هو البدائية الوحيدة المدعومة التي تدعم الأجهزة GPU (يتم تقسيم البيانات غير الثلاثية في مستوى السائق ، وهو غير فعال في تقديم في الوقت الحقيقي)

{{% alert color="primary" %}}

In هذا الإصدار نحن مثلثات فقط المضلعات لأنه مطلوب من قبل 3ds تصدير الملفات ، يتم فقدان طبيعية/uvs وغيرها من عناصر فيرتكس خلال هذا الإجراء ، يمكننا تنفيذ هذا في المستقبل.

{{% /alert %}}

في هذا المثال ، نقوم بتثليث شبكة من خلال استيراد ملف FBX وحفظه بتنسيق FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **إنشاء مشهد مكعبات 3D**
يوضح هذا الموضوع كيفية إضافة هندسة شبكية إلى مشهد 3D. يضع رمز المثال مكعبًا ويحفظ مشهد 3D في تنسيقات الملفات المدعومة.
###  **Rereate Cube oode**
عقدة A غير مرئية ، ولكن يمكن تقديم الهندسة المرفقة بالعقدة.

{{% alert color="primary" %}}

يتم استخدام كائن فئة الشبكة في الرمز. يمكننا [إنشاء كائن فئة `Mesh` كما روى هناك](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Example**

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Add Node to a scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "CubeScene.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7400ASCII)

{{< /highlight >}}

{{% alert color="primary" %}}

ملاحظة: عادة ما يتم تجاهل الكيانات المرتبطة بعقدة الجذر في برامج CAM/CAD ، لذلك نحتاج إلى إنشاء عقدة جديدة لعرض الشكل الهندسي.

{{% /alert %}}
