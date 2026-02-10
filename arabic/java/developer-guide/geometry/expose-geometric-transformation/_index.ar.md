---
title: Ranxpose ranمقياس التيار الكهربائي
type: docs
weight: 50
url: /ar/java/expose-geometric-transformation/
description: Aspose.3D for Java يسمح بعرض التحول الهندسي لمشهد 3D. يمكنك تقييم التحول العالمي باستخدام طريقة التقييم lobalconversion.
---
#  **Ranxpose ranمقياس التيار الكهربائي**
Aspose.3D for Java يسمح بعرض التحول الهندسي لمشهد 3D. يمكنك تقييم التحول العالمي باستخدام طريقة `evaluateGlobalTransform`. يوضح مقتطف الشفرة التالي كيفية فضح التحول الهندسي.

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
