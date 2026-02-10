---
title: Fügen Sie Knoten hierarchie hinzu und teilen Sie geometrische Daten von Mesh unter mehreren Knoten der 3D-Szene
type: docs
weight: 40
url: /de/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET bietet an, eine Knoten hierarchie zu erstellen. Der Knoten ist der grundlegende Baustein einer Szene. Eine Knoten hierarchie definiert die logische Struktur einer Szene und liefert sichtbare Inhalte, indem Geometrien, Lichter und Kameras an Knoten angebracht werden.
---
##  **Knoten hierarchie in 3D Szenen dokument hinzufügen**
Aspose.3D for Python via .NET bietet an, eine Knoten hierarchie zu erstellen. Der Knoten ist der grundlegende Baustein einer Szene. Eine Knoten hierarchie definiert die logische Struktur einer Szene und liefert sichtbare Inhalte, indem Geometrien, Lichter und Kameras an Knoten angebracht werden.
###  **Szenen-Grafik-Beispiel**
Eine Beispiel-Szenen hierarchie sieht so aus:

! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

In Aspose.3D kann jede `Node`-Instanz mehrere unter geordnete Knoten haben. In diesem Beispiel haben wir einen Knoten mit zwei Würfel knoten erstellt. Wenn wir den Stamm knoten drehen, sind auch alle unter geordneten Knoten betroffen:

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
##  **Teilen Sie die Geometrie daten von Mesh zwischen mehreren Knoten**
Um den Speicher bedarf zu verringern, kann eine einzelne Instanz der [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh)-Klasse an verschiedene Instanzen der [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node)-Klasse gebunden werden. Stellen Sie sich vor, dass Sie ein System benötigen, in dem alle 3D Würfel nicht zu unterscheiden schienen, aber Sie benötigten zahlreiche viele davon. Sie können Speicher platz sparen, indem Sie ein Mesh-Objekt erstellen, wenn das System gestartet wird. An diesem Punkt erstellen Sie jedes Mal, wenn Sie eine andere Form benötigen, ein anderes Knoten objekt und zeigen diesen Knoten auf das eine Mesh. Dies wird als Instancing bezeichnet. Aspose.3D for Python via .NET APIs erlauben Instancing.
###  **Instancing Beispiel**
In den RTS-Spielen (Echtzeit strategie) wie können wir immer mehrere NPCs (Non-Player Character) mit demselben 3D-Modell sehen, möglicher weise in verschiedenen Farben. Die Rendering-Engine teilt normaler weise dieselben Mesh-Geometrie-Daten über verschiedene NPCs hinweg wird Instancing genannt.

{{% alert color="primary" %}}

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein `Mesh`-Klassen objekt, wie es dort erzählt wird](/3d/de/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demonstration des Beispiel codes:

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

In diesem Beispiel haben wir 3 Würfel knoten erstellt, die dasselbe Netz haben. Jeder von ihnen hat unterschied liches Material mit unterschied lichen Farben.
