---
title: Expose eoeometrik Transformation
type: docs
weight: 50
url: /tr/java/expose-geometric-transformation/
description: Aspose.3D for Java, 3D sahnesinin geometrik dönüşümünü açığa çıkarmanıza izin verir. Evaluateglobaltransform yöntemini kullanarak küresel dönüşümü değerlendirebilirsiniz.
---
#  **Expose eoeometrik Transformation**
Aspose.3D for Java, 3D sahnesinin geometrik dönüşümünü açığa çıkarmanıza izin verir. Global dönüşümü `evaluateGlobalTransform` yöntemiyle değerlendirebilirsiniz. Aşağıdaki kod parçacığı, geometrik dönüşümün nasıl ortaya çıkacağını gösterir.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize node
Node n = new Node();
// Get Geometric Translation
n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));
// The first Console.WriteLine will output the transform matrix that includes the geometric transformation
// while the second one will not.
System.out.println(n.evaluateGlobalTransform(true));
System.out.println(n.evaluateGlobalTransform(false));

{{< /highlight >}}
