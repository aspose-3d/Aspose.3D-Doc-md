---
title: Exponer la transformación geométrica
type: docs
weight: 80
url: /es/net/expose-geometric-transformation/
description: Aspose.3D for .NET permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método EvaluateGlobalTransform.
---
##  **Exponer la transformación geométrica**
Aspose.3D for .NET permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método `EvaluateGlobalTransform`. El siguiente fragmento de código muestra cómo exponer la transformación geométrica.

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
