---
title: Ställ in normalvärden eller UV på kuben och Lägg till material till 3D Enheter
type: docs
weight: 20
url: /sv/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Hur man skapar normal- eller uv-data på en mesh i Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex är dess position i rymden och dess normala, en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar. Normalerna bör vara enhetsvektorer. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2d-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.

{{% /alert %}} {{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan [Skapa ett klassobjekt `Mesh` som berättat där.](/3d/sv/python-net/create-3d-mesh-and-scene/) och sedan peka nod till Mesh geometri med [Skapa en 3D Scene](/3d/sv/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Skapa normala vektorer**
För att ha en bra visuell utseende på belysning, måste vi specificera normaler information för varje vertex, att ha en bättre detaljer, vi kan också använda normal och diffus karta (säkra att du kan använda skugg/spekular karta) för att utföra per-pixel normal/färg. En pervertex-information som normal eller vertex färg uppnås av `VertexElement`. I Aspose. 3D kan vi kartlägga extra information till kontrollpunkter/polygon vertex/polygon/kant, ett prov för att definiera normaler för vertex:

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

De 8 normala vektorerna är mappade till 8 styrpunkter direkt, i nästa exempel, kommer vi att demonstrera lite mer komplext scenario.
##  **Skapa UV- koordinater**
Här har vi endast definierat 4 UV-koordinater, men tillämpade dem till 24 polygon hörn (6 face * 4 vertex per polygon) genom att använda index.
Aspose.3D tillhandahåller 5 kartläggningslägen:

- `CONTROL_POINT` - Varje data mappas till geometriens styrpunkt.
- `POLYGON_VERTEX` - Uppgifterna är mappade till polygonens vertex.
- `POLYGON` - Uppgifterna är mappade till polygonen.
- `EDGE` - Uppgifterna är mappade till kanten.
- `ALL_SAME` - en data mappad till hela geometrin.



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
##  **Lägg till material till 3D Objekt**
Aspose.3D for Python via .NET låter utvecklare använda skuggaalgoritm för exakt skuggning och markeringar. Phong har flera karta ingångar som vi kan använda för att dölja effekten till noden. Fysiskt baserad rendering (PBR) tar hänsyn till vissa fysiska egenskaper hos objekt, ett sådant tillvägagångssätt ger utseendet av material som i den verkliga världen.
###  **Phong Material med textur för kub**
När UV-koordinaterna är färdiga att använda, kan vi applicera en textur på ytan av nät med hjälp av material. Endast vertex färg kan inte beskriva ytans detaljer, det är vad material används för. Här är ett exempel för att bifoga ett Phong-material till kubennoden:

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

Vi specificerade den diffusa texturkartläggningen, och en spekulär färg med en lysande parameter.
###  **Applicera fysiskt baserat renderingsmaterial (PBR) på en låd**
PBR spelar en nyckelroll för spelmotorns visuella, med sin effektiva och realistiska återgivning av växelverkan mellan ljus och yta genom att dämpa ljusstyrkan och spridning av reflekterat ljus. .. Utvecklare kan använda Aspose.3D API för att applicera PBR-material på 3D-objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan tillämpar PBR-materialet.

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
