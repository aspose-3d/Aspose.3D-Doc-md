---
title: Exponera geometrisk omvandling
type: docs
weight: 80
url: /sv/net/expose-geometric-transformation/
description: Aspose.3D for .NET tillåter exponering av geometrisk transformation av en 3D scen. Du kan utvärdera den globala transformationen med hjälp av EvaluateGlobalTransform metod.
---
##  **Exponera geometrisk omvandling**
Aspose.3D for .NET tillåter exponering av geometrisk transformation av en 3D scen. Du kan utvärdera den globala transformationen med `EvaluateGlobalTransform`-metoden. Följande kodsnutt visar hur man exponerar den geometriska transformationen.

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
