---
title: Exponer la transformación geométrica
type: docs
weight: 50
url: /es/java/expose-geometric-transformation/
description: Aspose.3D for Java permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método evaluateGlobalTransform.
---
#  **Exponer la transformación geométrica**
Aspose.3D for Java permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método `evaluateGlobalTransform`. El siguiente fragmento de código muestra cómo exponer la transformación geométrica.

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
