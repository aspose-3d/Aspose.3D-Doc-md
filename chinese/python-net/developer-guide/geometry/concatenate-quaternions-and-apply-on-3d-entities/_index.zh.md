---
title: 连接四元数并应用于3D实体
type: docs
weight: 50
url: /zh/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D Python via .NET允许开发人员将两个旋转变换组合成四元数中表示的一个。
---
{{% alert color="primary" %}} 

[Aspose.3D为Python via .NET](https://www.aspose.com/products/3d)允许开发人员将两个旋转变换组合成一个四元数表示的变换。

{{% /alert %}} 
## **级联四元数**
四元数用于表示3D空间中的方向。[`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion)类公开的`concat`方法可用于组合两个四元数。在这个代码示例中，我们将两个四元数组合在一起，得到第三个生成的四元数，然后将这三个四元数应用于三个圆柱体。
### **编程示例**
此代码示例将两个四元数组合在一起，并将它们应用于不同的圆柱体。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-ConcatenateQuaternions-ConcatenateQuaternions.py" >}}


**结果3ds MAX**

![todo: 图像_alt_文本](concatenate-quaternions-and-apply-on-3d-entities_1.png)
