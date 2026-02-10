---
title: Aggiunta della trasformazione al nodo
type: docs
weight: 30
url: /it/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe Transform per accedere a questi in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET offre la possibilità di ruotare gli oggetti in 3D spazio. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Traduzione/Scaling/Rotazione) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe `Transform` per accedere a questi in Aspose.3D. Le trasformazioni affini includono:

- Traduzione
- Scalatura
- Rotazione
- Mappatura del taglio
- Spremi la mappatura

{{% alert color="primary" %}}

L'oggetto della classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) viene utilizzato nel codice. Possiamo [Creare un oggetto di classe `Mesh` come narrato lì](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Ruota da Quaternion**
{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.utilities import Quaternion, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Set rotation
cubeNode.transform.rotation = Quaternion.from_rotation(Vector3(0, 1, 0), Vector3(0.3, 0.5, 0.1))
#  Set translation
cubeNode.transform.translation = Vector3(0, 0, 20)
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "TransformationToNode.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Ruota per angoli di Eulero**
{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Euler angles
cubeNode.transform.euler_angles = Vector3(0.3, 0.1, -0.5)
#  Set translation
cubeNode.transform.translation = Vector3(0, 0, 20)
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "TransformationToNode.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Matrice di trasformazione personalizzata**
Possiamo anche usare Matrix direttamente:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.utilities import Matrix4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Set custom translation matrix
cubeNode.transform.transform_matrix = Matrix4(1, -0.3, 0, 0, 0.4, 1, 0.3, 0, 0, 0, 1, 0, 0, 20, 0, 1
)
#  Add cube to the scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "TransformationToNode.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
