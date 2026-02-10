---
title: Expose Geometric Transformation
type: docs
weight: 80
url: /net/expose-geometric-transformation/
description: Aspose.3D for .NET allows exposing geometric transformation of a 3D scene. You can evaluate the global transformation using EvaluateGlobalTransform method.
---

## **Expose Geometric Transformation**
Aspose.3D for .NET allows exposing geometric transformation of a 3D scene. You can evaluate the global transformation using `EvaluateGlobalTransform` method. The following code snippet shows how to expose the geometric transformation.

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
