---
title: Exponera geometrisk omvandling
type: docs
weight: 80
url: /sv/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET tillåter exponering av geometrisk transformation av en 3D scen. Du kan utvärdera den globala transformationen med hjälp av EvaluateGlobalTransform metod.
---
#  **Exponera geometrisk omvandling**
Aspose.3D for Python via .NET tillåter exponering av geometrisk transformation av en 3D scen. Du kan utvärdera den globala transformationen med `evaluateGlobalTransform`-metoden. Följande kodsnutt visar hur man exponerar den geometriska transformationen.

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
