---
title: 3D Mesh und Szene erstellen
type: docs
weight: 10
url: /de/python-net/create-3d-mesh-and-scene/
description: Ein Netz wird durch eine Reihe von Kontroll punkten und die vielen n-seitigen Polygone nach Bedarf definiert. Dieser Artikel erklärt, wie man ein Mesh definiert.
---
##  **Erstellen Sie ein 3D Cube Mesh**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) wird durch eine Reihe von Kontroll punkten und die vielen n-seitigen Polygone nach Bedarf definiert. Dieser Artikel erklärt, wie man ein Mesh definiert.

Um eine Mesh-Oberfläche zu erstellen, müssen wir Kontroll punkte und Polygone wie folgt definieren:

- [Definieren Sie die Kontroll punkte](/3d/de/python-net/create-3d-mesh-and-scene/)
- [Erstellen Sie Polygone mit der PolygonBuilder-Klasse](/3d/de/python-net/create-3d-mesh-and-scene/)
- [Polygone erstellen](/3d/de/python-net/create-3d-mesh-and-scene/)

Hier ist ein Beispiel zum Anhängen eines Phong-Materials an den Würfel knoten:
###  **Definieren Sie die Kontroll punkte**
Ein Netz besteht aus einer Reihe von Kontroll punkten im Raum und Polygonen, um die Netz oberfläche zu beschreiben. Um ein Netz zu erstellen, müssen wir die Kontroll punkte definieren:

{{% alert color="primary" %}}

Die Kontroll punkte aller Geometrien in Aspose.3D verwenden eine homogene Koordinate, also `Vector4` statt `Vector3` im Beispiel code.

{{% /alert %}}

**Beispiel:**

{{< highlight "python" >}}
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize control points
controlPoints = [Vector4(-5.0, 0.0, 5.0, 1.0), Vector4(5.0, 0.0, 5.0, 1.0), Vector4(5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 0.0, -5.0, 1.0), Vector4(5.0, 0.0, -5.0, 1.0), Vector4(5.0, 10.0, -5.0, 1.0), Vector4(-5.0, 10.0, -5.0, 1.0)]

{{< /highlight >}}


###  **Polygone erstellen**
Die Kontroll punkte sind nicht render ierbar. Um den Würfel sichtbar zu machen, müssen wir Polygone auf jeder Seite definieren:

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


###  **Erstellen Sie Polygone mit der PolygonBuilder-Klasse**
Wir können Polygon auch durch Eckpunkte mit der `PolygonBuilder`-Klasse definieren:

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

Jetzt ist es fertig, um das Netz sichtbar zu machen, müssen wir einen Knoten dafür vorbereiten.
##  **Wie man ein Netz trianguliert**
Triangulate Mesh ist für die Spiele industrie nützlich, da das Dreiecksnetz das einzige unterstützte Primitiv ist, das die GPU-Hardware unterstützt (nicht dreieckige Daten werden auf Treiber ebene trianguliert, was beim Echtzeit-Rendering ineffizient ist).

{{% alert color="primary" %}}

In dieser Version haben wir die Polygone nur trianguliert, da dies für den Export von 3ds-Dateien erforderlich ist. Normalen/Uvs und andere Scheitel punkt elemente gehen während dieses Verfahrens verloren. Wir können dies in Zukunft implemen tieren.

{{% /alert %}}

In diesem Beispiel triangulieren wir ein Mesh, indem wir eine FBX-Datei importieren und im FBX-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **Erstellen Sie eine 3D Cube-Szene**
Dieses Thema zeigt, wie Mesh-Geometrie zur 3D-Szene hinzugefügt wird. Der Beispielcode platziert einen Cube und speichert 3D Szene in den unterstützten Dateiformaten.
###  **Erstellen Sie einen Würfel knoten**
Ein Knoten ist unsichtbar, aber die an den Knoten angehängte Geometrie kann gerendert werden.

{{% alert color="primary" %}}

Das Mesh-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein `Mesh`-Klassen objekt, wie es dort erzählt wird](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Beispiel**

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

HINWEIS: Die an den Stamm knoten angehängten Entitäten werden normaler weise in CAD/CAM-Softwares ignoriert. Daher müssen wir einen neuen Knoten erstellen, um die Geometrie zu rendern.

{{% /alert %}}
