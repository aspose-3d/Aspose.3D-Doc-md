---
title: NNNransformation to the Node
type: docs
weight: 30
url: /tr/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class Transform to access these in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET offers to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) class.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class `Transform` to access these in Aspose.3D. Affine transformations include:

- Translation
- Scaling
- Rotation
- Shear haritalama
- Squeeze haritalama

{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Qotate by uuaternion**
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
##  **Eotate by Euler ngngles**
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
##  **Custom formation ransformation Matrix**
We ayrıca doğrudan Matrix kullanabilir:

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
