---
title: Настройте нормали или УФ на Кубе и добавьте материал в сущности 3D
type: docs
weight: 20
url: /ru/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Как создать нормали или uv данные на сетке в Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET предлагает управлять нормалями и УФ на геометрических фигурах. Сетка хранит ключевые свойства для каждой вершины-ее положение в пространстве и нормаль, вектор, перпендикулярный исходной поверхности. Нормальный является основным для количества затенений. Нормали должны быть единичными векторами. Большинство форматов сетки также поддерживают некоторую форму УФ-координат, которые представляют собой отдельное 2d представление сетки, «развернутой», чтобы показать, какую часть двумерной текстурной карты применять к различным полигонам сетки.

{{% /alert %}} {{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса `Mesh`, как там рассказано](/3d/ru/python-net/create-3d-mesh-and-scene/), а затем указать узел на геометрию Mesh с помощью [Создание сцены 3D](/3d/ru/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Создание нормальных векторов**
Чтобы иметь хороший визуальный вид на освещение, нам нужно указать нормальную информацию для каждой вершины, чтобы иметь лучшие детали, мы также можем использовать нормальную и диффузную карту (конечно, вы можете использовать теневую/зеркальную карту) для выполнения на пиксель нормаль/цвет. Информация для каждой вершины, такая как нормальный цвет или цвет вершины, достигается с помощью `VertexElement`. В Aspose.3D мы можем сопоставить дополнительную информацию с контрольными точками/вершинами полигона/полигонов/ребром, выборкой для определения нормалей для вершины:

{{< highlight "python" >}}
from aspose import pycore
from aspose.threed.entities import MappingMode, ReferenceMode, VertexElementNormal, VertexElementType
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Raw normal data
normals = [Vector4(-0.577350258, -0.577350258, 0.577350258, 1.0), Vector4(0.577350258, -0.577350258, 0.577350258, 1.0), Vector4(0.577350258, 0.577350258, 0.577350258, 1.0), Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0), Vector4(-0.577350258, -0.577350258, -0.577350258, 1.0), Vector4(0.577350258, -0.577350258, -0.577350258, 1.0), Vector4(0.577350258, 0.577350258, -0.577350258, 1.0), Vector4(-0.577350258, 0.577350258, -0.577350258, 1.0)]
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
normal = mesh.create_element(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT)
elementNormal = pycore.as_of(normal, VertexElementNormal) if pycore.is_assignable(normal, VertexElementNormal) else None
#  Copy the data to the vertex element
elementNormal.data.extend(normals)

{{< /highlight >}}

8 нормальных векторов сопоставляются с 8 контрольными точками напрямую, в следующем примере мы продемонстрируем немного более сложный сценарий.
##  **Создание УФ-координат**
Здесь мы определили только 4 УФ-координаты, но применили их к 24 вершинам многоугольника (6 грани * 4 вершины на многоугольник) с помощью индексов.
Aspose.3D предоставляет 5 режимов сопоставления:

- `CONTROL_POINT` -все данные сопоставляются с контрольной точкой геометрии.
- `POLYGON_VERTEX` -данные отображаются в вершину многоугольника.
- `POLYGON` -данные сопоставлены с многоугольником.
- `EDGE` -данные сопоставлены с ребром.
- `ALL_SAME` -один из данных сопоставлен со всей геометрией.



{{< highlight "python" >}}
from aspose.threed.entities import MappingMode, ReferenceMode, TextureMapping
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  UVs
uvs = [Vector4(0.0, 1.0, 0.0, 1.0), Vector4(1.0, 0.0, 0.0, 1.0), Vector4(0.0, 0.0, 0.0, 1.0), Vector4(1.0, 1.0, 0.0, 1.0)]
#  Indices of the uvs per each polygon
uvsId = [    0, 1, 3, 2, 2, 3, 5, 4, 4, 5, 7, 6, 6, 7, 9, 8, 1, 10, 11, 3, 12, 0, 2, 13
]
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Create UVset
elementUV = mesh.create_element_uv(TextureMapping.DIFFUSE, MappingMode.POLYGON_VERTEX, ReferenceMode.INDEX_TO_DIRECT)
#  Copy the data to the UV vertex element
elementUV.data.extend(uvs)
elementUV.indices.extend(uvsId)

{{< /highlight >}}
##  **Добавить материалы в объекты 3D**
Aspose.3D for Python via .NET позволяет разработчикам использовать алгоритм затенения для точного затенения и подсвечивания. Фонг имеет несколько входов карты, которые мы можем использовать для маскировки эффекта для узла. Физически ориентированный рендеринг (PBR) учитывает некоторые физические свойства объектов, такой подход обеспечивает внешний вид материалов, как в реальном мире.
###  **Материал Phong с текстурой для куба**
Когда УФ-координаты готовы к использованию, мы можем нанести текстуру на поверхность сетки, используя материал. Только цвет вершины не может описать детали поверхности, это то, для чего использовались материалы. Вот пример для прикрепления материала Фонга к узлу куба:

{{< highlight "python" >}}
from aspose.pydrawing import Color
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.shading import PhongMaterial, Texture
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize cube node object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the mesh
cubeNode.entity = mesh
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  Initiallize PhongMaterial object
mat = PhongMaterial()
#  Initiallize Texture object
diffuse = Texture()
#  The path to the documents directory.
#  Set local file path
diffuse.file_name = "out"  + "surface.dds"
#  Set Texture of the material
mat.set_texture("DiffuseColor", diffuse)
#  Embed raw content data to FBX (only for FBX and optional)
#  Set file name
diffuse.file_name = "embedded-texture.png"
#  Set binary content
diffuse.content = open("data-dir"  + "aspose-logo.jpg", "rb").read()
#  Set color
mat.specular_color = Vector3(Color.red)
#  Set brightness
mat.shininess = 100.0
#  Set material property of the cube object
cubeNode.material = mat
output = "out"  + "MaterialToCube.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7400ASCII)

{{< /highlight >}}

Мы указали отображение диффузной текстуры и зеркальный цвет с параметром сияния.
###  **Применить материал для физического отендинга (PBR) к коробке**
PBR играет ключевую роль в визуальных эффектах игрового движка с его эффективной и реалистичной визуализацией взаимодействий между светом и поверхностью посредством ослабления яркости и рассеяния отраженного света. Разработчики могут использовать Aspose.3D API, чтобы применить материал PBR к 3D объектам в сцене. Этот пример кода демонстрирует, как создать объект Box, а затем применить материал PBR.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
