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
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
##  **按欧拉角旋转**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
##  **自定义转换矩阵**
我们也可以直接使用矩阵:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
