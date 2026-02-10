---
title: Ranxpose ranمقياس التيار الكهربائي
type: docs
weight: 80
url: /ar/net/expose-geometric-transformation/
description: Aspose.3D for .NET يسمح بعرض التحول الهندسي لمشهد 3D. يمكنك تقييم التحول العالمي باستخدام طريقة التقييم lobalconversion.
---
##  **Ranxpose ranمقياس التيار الكهربائي**
Aspose.3D for .NET يسمح بعرض التحول الهندسي لمشهد 3D. يمكنك تقييم التحول العالمي باستخدام طريقة `EvaluateGlobalTransform`. يوضح مقتطف الشفرة التالي كيفية فضح التحول الهندسي.

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
