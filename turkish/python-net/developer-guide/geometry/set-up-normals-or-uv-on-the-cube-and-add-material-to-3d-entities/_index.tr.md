---
title: Set up normals or UV on the Cube and Add Material to 3D Entities
type: docs
weight: 20
url: /tr/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Aspose içinde bir ağ üzerinde normaller veya uv verileri nasıl oluşturulur. 3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET geometrik şekillerde normalleri ve uv'yi yönetmeyi teklif eder. Bir ağ, her bir verteksin temel özelliklerini depolar, uzayda konumu ve normal, orijinal yüzeye dik bir vektör. Normal, sayıları gölgelendirmek için önemlidir. Normaller birim vektörleri olmalıdır. Çoğu örgü biçimi, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2d gösterimi olan bir uv koordinatlarını da destekler.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by [Creating a 3D Scene](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Create Normal ctors ectors**
Aydınlatma konusunda iyi bir görsel görünüme sahip olmak için, her vertex için normaller bilgilerini belirtmemiz, daha iyi bir ayrıntıya sahip olmamız gerekiyor, ayrıca normal ve dağınık haritayı da kullanabiliriz (gölge/speküler haritasını kullanabileceğinizden emin olun)-piksel başına normal/renk. Normal veya vertex rengi gibi bir vertex bilgisi `VertexElement` ile elde edilir. Aspose.3D vertex/polygon/edge noktalarını kontrol etmek için ekstra bilgileri haritalayabiliriz, vertex için normalleri tanımlamak için bir örnek:

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

The 8 normal vektör, 8 kontrol noktasına doğrudan eşleştirilir, bir sonraki örnekte, biraz daha karmaşık bir senaryo göstereceğiz.
##  **Create UV ordinoordinates**
Here, sadece 4 UV koordinatlarını tanımladık, ancak endeksleri kullanarak 24 poligon dikeyine (poligon başına 6 yüz * 4 vertex) uyguladık.
Aspose.3D 5 haritalama modu sağlar:

- `CONTROL_POINT` -her veri geometrinin kontrol noktasına eşleştirilir.
- `POLYGON_VERTEX` -veriler poligon'un vertex'ine eşleştirildi.
- `POLYGON` -veriler çokgen ile eşleştirilir.
- `EDGE` -veriler kenara yazılmıştır.
- `ALL_SAME` -tüm geometriye bir veri eşleştirildi.



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
##  **Add Materials to 3D Objects**
Aspose.3D for Python via .NET, geliştiricilerin doğru gölgeleme ve vurgular için gölgeleme algoritmasını kullanmasına izin verir. Phong, düğümün etkisini maskelemek için kullanabileceğimiz birkaç harita girişine sahiptir. Fiziksel olarak dayalı render (pbr) nesnelerin bazı fiziksel özelliklerini dikkate alır, bu tür bir yaklaşım gerçek dünyada olduğu gibi malzemelerin görünümünü sağlar.
###  **Cube için Texture ile Phong erial aterial**
Uhen Ucoordinates koordinatları kullanıma hazır, malzeme kullanarak örgü yüzeyine bir doku uygulayabiliriz. Only vertex rengi, yüzey detaylarını tarif edemez, bu da kullanılan malzemelerdir. Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:

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

We dağınık doku haritalama ve parlaklık parametresi ile speküler bir renk belirledi.
###  **Hyhycally hysically Based dering en( (PBR) erial aterial to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

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
