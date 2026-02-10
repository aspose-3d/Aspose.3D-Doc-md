---
title: Ersetzen Sie geometrische Transformation
type: docs
weight: 80
url: /de/net/expose-geometric-transformation/
description: Aspose.3D for .NET ermöglicht die Aufdeckung der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mithilfe der Evaluate Global Transform-Methode bewerten.
---
##  **Ersetzen Sie geometrische Transformation**
Aspose.3D for .NET ermöglicht die Aufdeckung der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mit der `EvaluateGlobalTransform` Methode auswerten. Das folgende Code-Snippet zeigt, wie die geometrische Transformation verfügbar gemacht wird.

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
