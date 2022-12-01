---
title: 向节点添加转换
type: docs
weight: 30
url: /zh/net/adding-transformation-to-the-node/
description: TSR (平移/缩放/旋转) 在3D场景中最常用，我们提供了一个类转换来Aspose.3D访问这些。
---
{{% alert color="primary" %}}

Aspose.3D for .NET提供在3D空间中旋转对象。有三种方法来定义对象在3D空间中的旋转，欧拉角，四元数和自定义矩阵，所有这些都由[`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform)类支持。

{{% /alert %}}

TSR (平移/缩放/旋转) 在3D场景中最常用，我们提供了一个类`Transform`来Aspose.3D访问这些。仿射变换包括:

- 翻译
- 缩放
- 旋转
- 剪切映射
- 挤压映射

{{% alert color="primary" %}}

代码中使用了[`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh)类对象。我们可以[创建一个网格类对象，如在那里叙述](/3d/zh/net/create-3d-mesh-and-scene/)。

{{% /alert %}}
## **按四元数旋转**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **按欧拉角旋转**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **自定义转换矩阵**
我们也可以直接使用矩阵:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
