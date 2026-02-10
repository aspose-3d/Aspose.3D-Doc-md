---
title: Set up normals or UV on the Cube and Add Material to 3D Entities
type: docs
weight: 20
url: /python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: How to create normals or uv data on a mesh in Aspose.3D.
---

{{% alert color="primary" %}}

Aspose.3D for Python via .NET offers to manage normals and UV on the geometric shapes. A mesh stores the key properties for every vertex are its position in space and its normal, a vector perpendicular to the original surface. The normal is major to shading counts. The normals should be unit vectors. Most mesh formats also support some form of UV coordinates which are a separate 2d representation of the mesh "unfolded" to show what portion of a 2-dimensional texture map to apply to different polygons of the mesh.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by [Creating a 3D Scene](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Create Normal Vectors**
To have a good visual look on lighting, we need to specify normals information for each vertex, to have a better details, we can also use normal and diffuse map (sure you can use shadow / specular map) to perform per-pixel normal/color. A per-vertex information like normal or vertex color is achieved by `VertexElement`. In Aspose.3D we can map extra information to control points/polygon vertex/polygon/edge, a sample to define normals for vertex:

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

The 8 normal vectors are mapped to 8 control points directly, in the next example, we’ll demonstrate a bit more complex scenario.
## **Create UV Coordinates**
Here,we only defined 4 UV coordinates, but applied them to 24 polygon vertices (6 face * 4 vertex per polygon) by using indices.
The Aspose.3D provides 5 mapping modes:

- `CONTROL_POINT` - each data is mapped to the control point of the geometry.
- `POLYGON_VERTEX` - the data is mapped to the polygon’s vertex.
- `POLYGON` - the data is mapped to the polygon.
- `EDGE` - the data is mapped to the edge.
- `ALL_SAME` - one data mapped to the whole geometry.



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
## **Add Materials to 3D Objects**
Aspose.3D for Python via .NET allows developers to use shading algorithm for accurate shading and highlights. The Phong has several map inputs which we can use to mask the effect to the node. Physically Based Rendering (PBR) takes some physical properties of objects into account, such an approach provides the appearance of materials as in the real world.
### **Phong Material with Texture for Cube**
When the UV coordinates are ready to use, we can apply a texture on the surface of mesh by using material. Only vertex color cannot describe the details of surface, that’s what materials used for. Here’s an example to attach a Phong material to the cube node:

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

We specified the diffuse texture mapping, and a specular color with a shininess parameter. 
### **Apply Physically Based Rendering (PBR) Material to a Box**
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
