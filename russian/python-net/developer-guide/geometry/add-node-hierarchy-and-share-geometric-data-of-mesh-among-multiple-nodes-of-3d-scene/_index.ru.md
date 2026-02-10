---
title: Добавить иерархию узлов и поделиться геометрическими данными сетки между несколькими узлами сцены 3D
type: docs
weight: 40
url: /ru/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET предлагает построить иерархию узлов. Узел является основным строительным блоком сцены. Иерархия узлов определяет логическую структуру сцены и обеспечивает видимый контент путем присоединения к узлам геометрии, источников света и камер.
---
##  **Добавить иерархию узлов в документе сцены 3D**
Aspose.3D for Python via .NET предлагает построить иерархию узлов. Узел является основным строительным блоком сцены. Иерархия узлов определяет логическую структуру сцены и обеспечивает видимый контент путем присоединения к узлам геометрии, источников света и камер.
###  **Пример графов сцены**
Образец иерархии сцен выглядит так:

! [Для: имаге_альт_текст](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

В Aspose.3D каждый экземпляр `Node` может иметь несколько дочерних узлов, в этом примере мы создали узел с двумя кубическими узлами, если мы повернем корневой узел, все дочерние узлы также будут затронуты:

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
##  **Поделитесь данными геометрии Mesh между несколькими узлами**
Чтобы уменьшить потребность в памяти, один экземпляр класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) может быть привязан к различным экземплярам класса [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node). Предположим, что вам нужна система, в которой все кубики 3D кажутся неразличимыми, но вам требуется большое количество из них. Вы можете сэкономить память, сделав один объект Mesh при старте системы. В этот момент каждый раз, когда вам требуется другая форма, вы делаете другой объект Node, а затем указываете этот узел на одну Mesh. Это называется инстанцирование. Aspose.3D for Python via .NET API позволяют выполнять инстрижку.
###  **Пример установки**
В таких играх, как RTS (стратегия в реальном времени), мы всегда можем увидеть несколько NPC (Non-Player Character) с одной и той же моделью 3D, возможно, в разных цветах, движок рендеринга обычно разделяет одни и те же данные геометрии сетки между разными NPC, этот метод называется Instancing.

{{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса `Mesh`, как там рассказано](/3d/ru/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Демонстрация кода примера:

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

В этом примере мы создали 3 кубических узла, которые имеют одну и ту же сетку, каждый из них имеет разный материал с разными цветами.
