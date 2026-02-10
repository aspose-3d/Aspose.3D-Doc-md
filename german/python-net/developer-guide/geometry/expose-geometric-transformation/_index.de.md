---
title: Ersetzen Sie geometrische Transformation
type: docs
weight: 80
url: /de/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET ermöglicht die Offenlegung der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mithilfe der Evaluate Global Transform-Methode bewerten.
---
#  **Ersetzen Sie geometrische Transformation**
Aspose.3D for Python via .NET ermöglicht die Offenlegung der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mit der `evaluateGlobalTransform` Methode auswerten. Das folgende Code-Snippet zeigt, wie die geometrische Transformation verfügbar gemacht wird.

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
