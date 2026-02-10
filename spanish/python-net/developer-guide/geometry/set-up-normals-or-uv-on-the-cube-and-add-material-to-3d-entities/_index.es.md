---
title: Configurar normales o UV en el cubo y agregar material a entidades 3D
type: docs
weight: 20
url: /es/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Cómo crear datos normales o uv en una malla en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET ofrece administrar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice son su posición en el espacio y su normal, un vector perpendicular a la superficie original. Lo normal es importante para los recuentos de sombreado. Las normales deben ser vectores unitarios. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2d separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.

{{% /alert %}} {{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos [Crear un objeto de clase `Mesh` como se narra allí](/3d/es/python-net/create-3d-mesh-and-scene/) y luego apuntar el nodo a la geometría de malla por [Creación de una escena 3D](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Crear vectores normales**
Para tener un buen aspecto visual en la iluminación, necesitamos especificar información de normales para cada vértice, para tener mejores detalles, también podemos usar mapa normal y difuso (seguro que puede usar mapa de sombra/especular) para realizar por píxel normal/color. Una información por vértice como el color normal o de vértice se logra mediante `VertexElement`. En Aspose.3D podemos asignar información adicional a los puntos de control/vértice del polígono/borde, una muestra para definir las normales para el vértice:

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

Los 8 vectores normales se asignan a 8 puntos de control directamente, en el siguiente ejemplo, demostraremos un escenario un poco más complejo.
##  **Crear coordenadas UV**
Aquí, solo definimos 4 coordenadas UV, pero las aplicamos a 24 vértices poligonales (6 caras * 4 vértices por polígono) mediante el uso de índices.
Aspose.3D proporciona 5 modos de asignación:

- `CONTROL_POINT` -cada dato se asigna al punto de control de la geometría.
- `POLYGON_VERTEX` -los datos se asignan al vértice del polígono.
- `POLYGON` -los datos se asignan al polígono.
- `EDGE` -los datos se asignan al borde.
- `ALL_SAME` -un dato asignado a toda la geometría.



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
##  **Agregar materiales a objetos 3D**
Aspose.3D for Python via .NET permite a los desarrolladores utilizar el algoritmo de sombreado para un sombreado y resaltados precisos. El Phong tiene varias entradas de mapa que podemos usar para enmascarar el efecto al nodo. Physically Based Rendering (PBR) tiene en cuenta algunas propiedades físicas de los objetos, tal enfoque proporciona la apariencia de los materiales como en el mundo real.
###  **Material Phong con textura para cubo**
Cuando las coordenadas UV están listas para usar, podemos aplicar una textura en la superficie de la malla utilizando material. Solo el color de los vértices no puede describir los detalles de la superficie, para eso se utilizaron los materiales. Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:

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

Especificamos el mapeo de textura difusa y un color especular con un parámetro de brillo.
###  **Aplicar material de rendering basado en la física (PBR) a una caja**
PBR juega un papel clave para las imágenes del motor del juego, con su representación eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar Aspose.3D API para aplicar material de PBR a objetos 3D en una escena. En este ejemplo de código se muestra cómo crear un objeto Box y, a continuación, aplicar el material PBR.

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
