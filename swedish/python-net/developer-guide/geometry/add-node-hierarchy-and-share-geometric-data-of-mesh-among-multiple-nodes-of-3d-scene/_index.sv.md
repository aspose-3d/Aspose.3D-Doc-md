---
title: Lägg till nodehierarki och Dela geometriska data av mesh bland flera noder i 3D Scene
type: docs
weight: 40
url: /sv/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET erbjuder att bygga en nodehierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
---
##  **Lägg till nodehierarki i 3D Scendokument**
Aspose.3D for Python via .NET erbjuder att bygga en nodehierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
###  **Exempel**
En provscen hierarki ser ut som:

![todo:image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

I Aspose. 3D, kan varje `Node` instans ha flera barnnoder, i detta exempel skapade vi en nod med två kubnoder, Om vi roterar rotnoden, alla barnnoder påverkas också:

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
##  **Dela meshs geometri data mellan flera noder**
För att minska minnesförnödenheter, kan en enda instans av [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) klass bindas till olika instanser av [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) klass. Föreställ dig att du behöver ett system där alla 3D kuber verkade vara oundvikliga, Men du krävde många av dem. Du kan spara minne genom att göra ett Mesh objekt när systemet börjar. Vid den punkten, varje gång du behövde en annan form, du gör en annan Node objekt, sedan peka den noden till en Mesh. Detta kallas instanser. Aspose.3D for Python via .NET API tillåter att göra instanser.
###  **Exempel**
I RTS (Real-time strategi) spel som, kan vi alltid se flera NPCs (Non-Player Character) med samma modell 3D, kanske i olika färger, renderingsmotorn brukar dela samma data för mashgeometri med olika NPC, Denna teknik kallas Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demonstration av exempelkod:

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

I detta exempel skapade vi 3 kub noder dela samma mesh, var och en av dem har olika material med olika färger.
