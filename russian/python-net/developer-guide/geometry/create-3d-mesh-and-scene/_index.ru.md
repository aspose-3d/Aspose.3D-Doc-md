---
title: Создать сетку и сцену 3D
type: docs
weight: 10
url: /ru/python-net/create-3d-mesh-and-scene/
description: Сетка определяется набором контрольных точек и множеством n-сторонних многоугольников по мере необходимости. В этой статье объясняется, как определить сетку.
---
##  **Создайте сетку-куб 3D**
[`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) определяется набором контрольных точек и множеством n-односторонних многоугольников по мере необходимости. Эта статья объясняет, как определить Mesh.

Чтобы создать поверхность сетки, нам нужно определить контрольные точки и полигоны следующим образом:

- [Определите контрольные точки](/3d/ru/python-net/create-3d-mesh-and-scene/)
- [Создайте многоугольники с классом PolygonBuilder](/3d/ru/python-net/create-3d-mesh-and-scene/)
- [Создание полигонов](/3d/ru/python-net/create-3d-mesh-and-scene/)

Вот пример для прикрепления материала Фонга к узлу куба:
###  **Определите контрольные точки**
Сетка состоит из набора контрольных точек в пространстве и полигонов для описания поверхности сетки, чтобы создать сетку, нам нужно определить контрольные точки:

{{% alert color="primary" %}}

В контрольных точках всех геометрий в Aspose.3D используется однородная координата, поэтому в примере это `Vector4` вместо `Vector3`.

{{% /alert %}}

**Пример:**

{{< highlight "python" >}}
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize control points
controlPoints = [Vector4(-5.0, 0.0, 5.0, 1.0), Vector4(5.0, 0.0, 5.0, 1.0), Vector4(5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 0.0, -5.0, 1.0), Vector4(5.0, 0.0, -5.0, 1.0), Vector4(5.0, 10.0, -5.0, 1.0), Vector4(-5.0, 10.0, -5.0, 1.0)]

{{< /highlight >}}


###  **Создание полигонов**
Контрольные точки не отображаются, чтобы сделать куб видимым, нам нужно определить полигоны в каждой стороне:

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


###  **Создайте многоугольники с классом PolygonBuilder**
Мы также можем определить многоугольник по вершинам с классом `PolygonBuilder`:

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

Теперь он закончен, чтобы сделать сетку видимой, нам нужно подготовить узел для нее.
##  **Как триангулировать сетку**
Треугольная сетка полезна для игровой индустрии, потому что треугольная-единственный поддерживаемый примитив, который поддерживает оборудование GPU (нетреугольные данные триангулированы на уровне драйвера, что неэффективно при рендеринге в реальном времени)

{{% alert color="primary" %}}

В этой версии мы только триангулировали полигоны, так как это требуется для экспорта файлов 3ds, нормали/uvs и другие элементы вершины теряются во время этой процедуры, мы можем реализовать это в будущем.

{{% /alert %}}

В этом примере мы триангулируем Mesh, импортируя файл FBX и сохраняем его в формате FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **Создайте сцену куба 3D**
В этом разделе показано, как добавить геометрию Mesh в сцену 3D. Пример кода помещает сцену куба и сохранения 3D в поддерживаемые форматы файлов.
###  **Создать узел куба**
Узел невидим, но можно визуализировать геометрию, прикрепленную к узлу.

{{% alert color="primary" %}}

В коде используется объект класса Mesh. Мы можем [Создать объект класса `Mesh`, как там рассказано](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Пример**

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

ПРИМЕЧАНИЕ: Сущности, прикрепленные к корневому узлу, обычно игнорируются в программном обеспечение CAD/CAM, поэтому нам нужно создать новый узел для рендеринга геометрии.

{{% /alert %}}
