---
title: 暴露几何变换
type: docs
weight: 80
url: /zh/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET 允许显示 3D 场景的几何变换。可以使用EvaluateGlobalTransform方法计算全局转换。
---
#  **暴露几何变换**
Aspose.3D for Python via .NET 允许显示 3D 场景的几何变换。您可以使用 `evaluateGlobalTransform` 方法计算全局转换。下面的代码段演示如何公开几何变换。

{{< highlight "python" >}}
from aspose.threed import Node
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize node
n = Node()
#  Get Geometric Translation
n.transform.geometric_translation = Vector3(10, 0, 0)
#  The first Console.WriteLine will output the transform matrix that includes the geometric transformation
#  while the second one will not.
print(n.evaluate_global_transform(True))
print(n.evaluate_global_transform(False))

{{< /highlight >}}
