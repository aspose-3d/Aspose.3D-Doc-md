---
title: Expose eoeometrik Transformation
type: docs
weight: 80
url: /tr/net/expose-geometric-transformation/
description: Aspose.3D for .NET, 3D sahnesinin geometrik dönüşümünü açığa çıkarmanıza izin verir. Evaluateglobaltransform yöntemini kullanarak küresel dönüşümü değerlendirebilirsiniz.
---
##  **Expose eoeometrik Transformation**
Aspose.3D for .NET, 3D sahnesinin geometrik dönüşümünü açığa çıkarmanıza izin verir. Global dönüşümü `EvaluateGlobalTransform` yöntemiyle değerlendirebilirsiniz. Aşağıdaki kod parçacığı, geometrik dönüşümün nasıl ortaya çıkacağını gösterir.

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
