---
title: Agregar jerarquía de nodos y compartir datos geométricos de malla entre múltiples nodos de 3D escena
type: docs
weight: 40
url: /es/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET ofrece la construcción de una jerarquía de nodos. El nodo es un bloque de construcción básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
---
##  **Agregar jerarquía de nodos en el documento de escena 3D**
Aspose.3D for Python via .NET ofrece la construcción de una jerarquía de nodos. El nodo es un bloque de construcción básico de una escena. Una jerarquía de nodos define la estructura lógica de una escena y proporciona contenido visible al unir geometrías, luces y cámaras a los nodos.
###  **Ejemplo de gráfico de escena**
Se parece a una jerarquía de escena de muestra:

¡! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

En Aspose.3D, cada instancia `Node` puede tener múltiples nodos hijos, en este ejemplo, creamos un nodo con dos nodos de cubo, si rotamos el nodo raíz, todos los nodos hijos también se ven afectados:

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
##  **Compartir datos de geometría de malla entre varios nodos**
Para disminuir las necesidades de memoria, una sola instancia de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class puede vincularse a varias instancias de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Supongamos que necesita un sistema en el que todos los 3D cubos parecían ser indistinguibles, sin embargo, requirió una gran cantidad de ellos. Podría ahorrar memoria haciendo un objeto Mesh cuando el sistema se inicie. En ese momento, cada vez que necesite otra forma, crea otro objeto Node y, a continuación, señala ese nodo a la Mesh. Esto se llama instanciación. Aspose.3D for Python via .NET Las APIs permiten hacer instanciación.
###  **Ejemplo de instalación**
En los juegos RTS (estrategia en tiempo real) como, siempre podemos ver múltiples NPC (personaje no jugador) con el mismo modelo 3D, tal vez en diferentes colores, el motor de renderizado generalmente comparte los mismos datos de geometría de malla en diferentes NPC, esta técnica se llama Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demostración del código de ejemplo:

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

En este ejemplo hemos creado 3 nodos de cubo que comparten la misma malla, cada uno de ellos tiene diferentes materiales con diferentes colores.
