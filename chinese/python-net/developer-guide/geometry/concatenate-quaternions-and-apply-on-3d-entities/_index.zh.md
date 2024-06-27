---
title: 连接四元数并应用于 3D 实体
type: docs
weight: 50
url: /zh/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Python via .NET 允许开发人员将两个旋转转换合并为一个以四元数表示的转换。
---
{{% alert color="primary" %}} 

[Aspose.3D for Python via .NET](https://www.aspose.com/products/3d) 允许开发人员将两个旋转转换合并为一个以四元数表示的转换。

{{% /alert %}} 
##  **级联四元数**
四元数用于表示 3D 空间中的方向。由 [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) 类公开的 `concat` 方法可用于组合两个四元数。在此代码示例中，我们组合两个四元数并获得第三个结果四元数，然后将这三个四元数应用于三个圆柱体。
###  **编程示例**
此代码示例将两个四元数组合在一起，并将它们应用于不同的圆柱体。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-ConcatenateQuaternions-ConcatenateQuaternions.py" >}}


**结果3ds MAX**

![todo: 图像 _ alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
