---
title: Esponi la trasformazione geometrica
type: docs
weight: 80
url: /it/net/expose-geometric-transformation/
description: Aspose.3D for .NET consente di esporre la trasformazione geometrica di una scena di 3D. È possibile valutare la trasformazione globale utilizzando il metodo EvaluateGlobalTransform.
---
##  **Esponi la trasformazione geometrica**
Aspose.3D for .NET consente di esporre la trasformazione geometrica di una scena di 3D. Puoi valutare la trasformazione globale usando il metodo `EvaluateGlobalTransform`. Il seguente frammento di codice mostra come esporre la trasformazione geometrica.

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
