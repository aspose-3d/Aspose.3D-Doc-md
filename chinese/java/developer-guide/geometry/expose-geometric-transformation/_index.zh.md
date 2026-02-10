---
title: 暴露几何变换
type: docs
weight: 50
url: /zh/java/expose-geometric-transformation/
description: Aspose.3D for Java 允许显示 3D 场景的几何变换。可以使用evaluateGlobalTransform方法计算全局转换。
---
#  **暴露几何变换**
Aspose.3D for Java 允许显示 3D 场景的几何变换。您可以使用 `evaluateGlobalTransform` 方法计算全局转换。下面的代码段演示如何公开几何变换。

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize node
Node n = new Node();
// Get Geometric Translation
n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));
// The first Console.WriteLine will output the transform matrix that includes the geometric transformation
// while the second one will not.
System.out.println(n.evaluateGlobalTransform(true));
System.out.println(n.evaluateGlobalTransform(false));

{{< /highlight >}}
