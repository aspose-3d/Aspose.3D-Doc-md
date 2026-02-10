---
title: Exponer la transformación geométrica
type: docs
weight: 80
url: /es/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método EvaluateGlobalTransform.
---
#  **Exponer la transformación geométrica**
Aspose.3D for Python via .NET permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método `evaluateGlobalTransform`. El siguiente fragmento de código muestra cómo exponer la transformación geométrica.

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
