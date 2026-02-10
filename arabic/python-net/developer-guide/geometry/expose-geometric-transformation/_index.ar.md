---
title: Ranxpose ranمقياس التيار الكهربائي
type: docs
weight: 80
url: /ar/python-net/expose-geometric-transformation/
description: يسمح Aspose.3D for Python via .NET بعرض التحول الهندسي لمشهد 3D. يمكنك تقييم التحول العالمي باستخدام طريقة التقييم lobalconversion.
---
#  **Ranxpose ranمقياس التيار الكهربائي**
يسمح Aspose.3D for Python via .NET بعرض التحول الهندسي لمشهد 3D. يمكنك تقييم التحول العالمي باستخدام طريقة `evaluateGlobalTransform`. يوضح مقتطف الشفرة التالي كيفية فضح التحول الهندسي.

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
