---
title: Crea mesh e scena 3D
type: docs
weight: 10
url: /it/python-net/create-3d-mesh-and-scene/
description: Una mesh è definita da un insieme di punti di controllo e da molti poligoni n-sided secondo necessità. Questo articolo spiega come definire una Mesh.
---
##  **Crea una mesh cubica da 3D**
Un [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) è definito da un insieme di punti di controllo e da molti poligoni n-sided, se necessario. Questo articolo spiega come definire una Mesh.

Per creare una superficie Mesh, dobbiamo definire i punti di controllo e i poligoni come segue:

- [Definire i punti di controllo](/3d/it/python-net/create-3d-mesh-and-scene/)
- [Crea poligoni con classe PolygonBuilder](/3d/it/python-net/create-3d-mesh-and-scene/)
- [Crea poligoni](/3d/it/python-net/create-3d-mesh-and-scene/)

Ecco un esempio per allegare un materiale Phong al nodo cubo:
###  **Definire i punti di controllo**
Una mesh è composta da un insieme di punti di controllo nello spazio e poligoni per descrivere la superficie della mesh, per creare una mesh, dobbiamo definire i punti di controllo:

{{% alert color="primary" %}}

I punti di controllo di tutte le geometrie in Aspose.3D utilizzano coordinate omogenee, quindi nel codice di esempio sono `Vector4` invece di `Vector3`.

{{% /alert %}}

**Esempio:**

{{< highlight "python" >}}
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize control points
controlPoints = [Vector4(-5.0, 0.0, 5.0, 1.0), Vector4(5.0, 0.0, 5.0, 1.0), Vector4(5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 0.0, -5.0, 1.0), Vector4(5.0, 0.0, -5.0, 1.0), Vector4(5.0, 10.0, -5.0, 1.0), Vector4(-5.0, 10.0, -5.0, 1.0)]

{{< /highlight >}}


###  **Crea poligoni**
I punti di controllo non sono renderabili, per rendere visibile il cubo, dobbiamo definire poligoni in ogni lato:

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


###  **Crea poligoni con classe PolygonBuilder**
Possiamo anche definire poligono per vertici con `PolygonBuilder` classe:

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

Ora è finito, per rendere visibile la mesh, dobbiamo preparare un nodo per questo.
##  **Come Triangolare una Mesh**
La mesh triangolata è utile per l'industria dei giochi perché il triangolare è l'unica primitiva supportata che l'hardware della GPU supporta (i dati non triangolari sono triangolati a livello di driver, il che è inefficiente nel rendering in tempo reale)

{{% alert color="primary" %}}

In questa versione abbiamo solo triangolato i poligoni poiché è richiesto dall'esportazione di file 3ds, normali/uvs e altri elementi vertici vengono persi durante questa procedura, possiamo implementarlo in futuro.

{{% /alert %}}

In questo esempio, triangolare una mesh importando FBX file e salvandolo in formato FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **Crea una scena del cubo 3D**
Questo argomento mostra come aggiungere la geometria mesh alla scena 3D. Il codice di esempio inserisce un cubo e salva 3D scena nei formati di file supportati.
###  **Creare un Nodo Cubo**
Un nodo è invisibile, ma è possibile eseguire il rendering della geometria collegata al nodo.

{{% alert color="primary" %}}

L'oggetto della classe Mesh viene utilizzato nel codice. Possiamo [Creare un oggetto di classe `Mesh` come narrato lì](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Esempio**

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

NOTA: le entità associate al nodo radice vengono solitamente ignorate nei software CAD/CAM, quindi è necessario creare un nuovo nodo per eseguire il rendering della geometria.

{{% /alert %}}
