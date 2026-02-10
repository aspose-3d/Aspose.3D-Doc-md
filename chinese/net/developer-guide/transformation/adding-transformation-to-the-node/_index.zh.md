---
title: 向节点添加转换
type: docs
weight: 30
url: /zh/net/adding-transformation-to-the-node/
description: TSR (平移/缩放/旋转) 在 3D 场景中最常用，我们在 Aspose.3D 中提供了一个类转换来访问这些。
---
{{% alert color="primary" %}}

Aspose。3D for .NET 提供在 3D 空间中旋转对象。有三种方法来定义对象在 3D 空间中的旋转，欧拉角，四元数和自定义矩阵，所有这些都由 [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) 类支持。

{{% /alert %}}

TSR (平移/缩放/旋转) 在 3D 场景中最常用，我们在 Aspose.3D 中提供了一个类 `Transform` 来访问这些。仿射变换包括:

- 翻译
- 缩放
- 旋转
- 剪切映射
- 挤压映射

{{% alert color="primary" %}}

代码中正在使用 [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) 类对象。我们可以 [创建一个网格类对象，如在那里叙述](/3d/zh/net/create-3d-mesh-and-scene/)。

{{% /alert %}}
##  **按四元数旋转**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
// Point node to the Mesh geometry
cubeNode.Entity = mesh;
// Set rotation
cubeNode.Transform.Rotation = Quaternion.FromRotation(new Vector3(0, 1, 0), new Vector3(0.3, 0.5, 0.1));            
// Set translation
cubeNode.Transform.Translation = new Vector3(0, 0, 20);            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            
   
// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
##  **按欧拉角旋转**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
// Point node to the Mesh geometry
cubeNode.Entity = mesh;
// Euler angles
cubeNode.Transform.EulerAngles = new Vector3(0.3, 0.1, -0.5);            
// Set translation
cubeNode.Transform.Translation = new Vector3(0, 0, 20);            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            

// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
##  **自定义转换矩阵**
我们也可以直接使用矩阵:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
// Point node to the Mesh geometry
cubeNode.Entity = mesh;
// Set custom translation matrix
cubeNode.Transform.TransformMatrix = new Matrix4(
1, -0.3, 0, 0,
0.4, 1, 0.3, 0,
0, 0, 1, 0,
0, 20, 0, 1
);        
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            
   
// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
