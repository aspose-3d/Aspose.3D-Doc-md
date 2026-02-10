---
title: Exposer la transformation géométrique
type: docs
weight: 80
url: /fr/net/expose-geometric-transformation/
description: Aspose.3D for .NET permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale à l'aide de la méthode EvaluateGlobalTransform.
---
##  **Exposer la transformation géométrique**
Aspose.3D for .NET permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale en utilisant la méthode `EvaluateGlobalTransform`. L'extrait de code suivant montre comment exposer la transformation géométrique.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize node 
var n = new Node();
// Get Geometric Translation
n.Transform.GeometricTranslation = new Vector3(10, 0, 0);
// The first Console.WriteLine will output the transform matrix that includes the geometric transformation 
// while the second one will not.
Console.WriteLine(n.EvaluateGlobalTransform(true));
Console.WriteLine(n.EvaluateGlobalTransform(false));

{{< /highlight >}}
