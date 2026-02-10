---
title: Richten Sie Normalen oder UV auf dem Würfel ein und fügen Sie Material zu 3D Entitäten hinzu
type: docs
weight: 20
url: /de/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: So erstellen Sie Normalen oder UV-Daten in einem Netz in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET bietet an, Normalen und UV auf die geometrischen Formen zu verwalten. Ein Netz speichert die Schlüssel eigenschaften für jeden Scheitel punkt, sind seine Position im Raum und seine Normalität, ein Vektor senkrecht zur ursprünglichen Oberfläche. Das Normale ist wichtig für die Schattierung zählt. Die Normalen sollten Einheits vektoren sein. Die meisten Netz formate unterstützen auch eine Form von UV-Koordinaten, bei denen es sich um eine separate 2D-Darstellung des "entfalteten" Netzes handelt, um zu zeigen, welcher Teil einer zwei dimensionalen Textur karte auf verschiedene Polygone des Netzes angewendet werden soll.

{{% /alert %}} {{% alert color="primary" %}}

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein `Mesh`-Klassen objekt, wie es dort erzählt wird](/3d/de/python-net/create-3d-mesh-and-scene/) und dann den Knoten um [Erstellen einer 3D-Szene](/3d/de/net/create-3d-mesh-and-scene/) auf die Mesh-Geometrie zeigen.

{{% /alert %}}
##  **Normale Vektoren erstellen**
Um ein gutes visuelles Aussehen der Beleuchtung zu haben, müssen wir Normale Informationen für jeden Scheitel punkt angeben, um bessere Details zu haben, können wir auch normale und diffuse Karte verwenden (sicher, dass Sie Schatten/spekulare Karte verwenden können), um pro Pixel normal/Farbe auszuführen. Eine Pro-Vertex-Information wie Normal-oder Scheitel punkt farbe wird durch `VertexElement` erreicht. In Aspose.3D können wir zusätzliche Informationen an Kontroll punkte/Polygon vertex/Polygon/Kante abbilden, ein Beispiel, um Normalen für Scheitel punkt zu definieren:

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

Die 8 normalen Vektoren werden direkt 8 Kontroll punkten zugeordnet. Im nächsten Beispiel werden wir ein etwas komplexeres Szenario demonstrieren.
##  **Erstellen von UV-Koordinaten**
Hier haben wir nur 4 UV-Koordinaten definiert, sie jedoch mithilfe von Indizes auf 24 Polygon scheitel punkte (6 Fläche * 4 Scheitel punkt pro Polygon) angewendet.
Die Aspose.3D bietet 5 Mapping-Modi:

- `CONTROL_POINT` -jede Daten wird dem Kontroll punkt der Geometrie zugeordnet.
- `POLYGON_VERTEX` -Die Daten werden dem Scheitel punkt des Polygons zugeordnet.
- `POLYGON` -die Daten werden dem Polygon zugeordnet.
- `EDGE` -die Daten werden dem Rand zugeordnet.
- `ALL_SAME` -eine Daten, die der gesamten Geometrie zugeordnet sind.



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
##  **Materialien zu 3D Objekten hinzufügen**
Aspose.3D for Python via .NET ermöglicht es Entwicklern, Shading-Algorithmus für genaue Schattierung und Highlights zu verwenden. Der Phong verfügt über mehrere Karten eingaben, mit denen wir den Effekt auf den Knoten maskieren können. Physically Based Rendering (PBR) berücksicht igt einige physikalische Eigenschaften von Objekten. Ein solcher Ansatz bietet das Erscheinung sbild von Materialien wie in der realen Welt.
###  **Phong Material mit Textur für Würfel**
Wenn die UV-Koordinaten einsatz bereit sind, können wir eine Textur auf die Oberfläche des Netzes anwenden, indem wir Material verwenden. Nur die Scheitel punkt farbe kann die Details der Oberfläche nicht beschreiben, dafür werden Materialien verwendet. Hier ist ein Beispiel zum Anhängen eines Phong-Materials an den Würfel knoten:

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

Wir haben die diffuse Textur abbildung und eine spiegele Farbe mit einem Glanz parameter angegeben.
###  **Wenden Sie physikalisch basiertes Rendering-Material (PBR) auf eine Box an**
PBR spielt eine Schlüssel rolle für die Game Engine-Grafik mit seiner effizienten und realistischen Darstellung von Wechsel wirkungen zwischen Licht und Oberfläche durch Dämpfung der Helligkeit und Streuung von reflektiertem Licht. Entwickler können Aspose.3D API verwenden, um PBR-Material auf 3D-Objekte in einer Szene anzuwenden. In diesem Code beispiel wird ver anschaulicht, wie ein Box-Objekt erstellt und anschließend das PBR-Material angewendet wird.

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
