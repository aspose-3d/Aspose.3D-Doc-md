---
title: 向节点添加转换
type: docs
weight: 30
url: /zh/python-net/adding-transformation-to-the-node/
description: TSR (平移/缩放/旋转) 在 3D 场景中最常用，我们在 Aspose.3D 中提供了一个类转换来访问这些。
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET 提供旋转 3D 空间中的对象。有三种方法来定义对象在 3D 空间中的旋转，欧拉角，四元数和自定义矩阵，所有这些都由 [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) 类支持。

{{% /alert %}}

TSR (平移/缩放/旋转) 在 3D 场景中最常用，我们在 Aspose.3D 中提供了一个类 `Transform` 来访问这些。仿射变换包括:

- 翻译
- 缩放
- 旋转
- 剪切映射
- 挤压映射

{{% alert color="primary" %}}

代码中正在使用 [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) 类对象。我们可以 [在此处创建一个 `Mesh` 类对象](/3d/zh/net/create-3d-mesh-and-scene/)。

{{% /alert %}}
##  **按四元数旋转**
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
##  **按欧拉角旋转**
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
##  **自定义转换矩阵**
我们也可以直接使用矩阵:

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
