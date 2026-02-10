---
title: Выяснить геометрическую трансформацию
type: docs
weight: 80
url: /ru/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET позволяет отображать геометрическое преобразование сцены 3D. Вы можете оценить глобальное преобразование с помощью метода EvaluateGlobalTransform.
---
#  **Выяснить геометрическую трансформацию**
Aspose.3D for Python via .NET позволяет отображать геометрическое преобразование сцены 3D. Вы можете оценить глобальную трансформацию, используя метод `evaluateGlobalTransform`. Следующий фрагмент кода показывает, как раскрыть геометрическое преобразование.

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
