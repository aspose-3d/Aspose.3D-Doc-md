---
title: Ajout de la transformation au nœud
type: docs
weight: 30
url: /fr/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe Transform pour y accéder dans Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET propose de faire pivoter des objets dans un espace 3D. Il existe trois façons de définir la rotation de l'objet dans l'espace 3D, les angles d'Euler, le quaternion et la matrice personnalisée, toutes sont supportées par la classe [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

Les TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe `Transform` pour y accéder dans Aspose.3D. Les transformations affines comprennent:

- Traduction
- Mise à l'échelle
- Rotation
- Cartographie de cisaillement
- Cartographie à presser

{{% alert color="primary" %}}

L'objet de classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est utilisé dans le code. Nous pouvons [Créer un objet de classe `Mesh` comme raconté là](/3d/fr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Tourner par Quaternion**
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
##  **Tourner par Euler Angles**
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
##  **Matrice de transformation personnalisée**
Nous pouvons également utiliser Matrix directement:

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
