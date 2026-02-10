---
title: Expose eoeometrik Transformation
type: docs
weight: 80
url: /tr/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET, 3D sahnesinin geometrik dönüşümünü açığa çıkarmanıza izin verir. Evaluateglobaltransform yöntemini kullanarak küresel dönüşümü değerlendirebilirsiniz.
---
#  **Expose eoeometrik Transformation**
Aspose.3D for Python via .NET, 3D sahnesinin geometrik dönüşümünü açığa çıkarmanıza izin verir. Global dönüşümü `evaluateGlobalTransform` yöntemiyle değerlendirebilirsiniz. Aşağıdaki kod parçacığı, geometrik dönüşümün nasıl ortaya çıkacağını gösterir.

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
