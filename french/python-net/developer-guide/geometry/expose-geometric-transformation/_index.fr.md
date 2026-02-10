---
title: Exposer la transformation géométrique
type: docs
weight: 80
url: /fr/python-net/expose-geometric-transformation/
description: Aspose.3D for Python via .NET permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale à l'aide de la méthode EvaluateGlobalTransform.
---
#  **Exposer la transformation géométrique**
Aspose.3D for Python via .NET permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale en utilisant la méthode `evaluateGlobalTransform`. L'extrait de code suivant montre comment exposer la transformation géométrique.

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
