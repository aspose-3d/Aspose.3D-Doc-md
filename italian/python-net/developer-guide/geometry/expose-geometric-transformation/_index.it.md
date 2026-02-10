---
title: Esponi la trasformazione geometrica
type: docs
weight: 80
url: /it/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET consente di esporre la trasformazione geometrica di una scena 3D. È possibile valutare la trasformazione globale utilizzando il metodo EvaluateGlobalTransform.
---
#  **Esponi la trasformazione geometrica**
Aspose.3D for Python via .NET consente di esporre la trasformazione geometrica di una scena 3D. Puoi valutare la trasformazione globale usando il metodo `evaluateGlobalTransform`. Il seguente frammento di codice mostra come esporre la trasformazione geometrica.

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
