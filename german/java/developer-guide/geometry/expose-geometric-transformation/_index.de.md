---
title: Ersetzen Sie geometrische Transformation
type: docs
weight: 50
url: /de/java/expose-geometric-transformation/
description: Aspose.3D for Java ermöglicht die Aufdeckung der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mithilfe der evaluate Global Transform-Methode bewerten.
---
#  **Ersetzen Sie geometrische Transformation**
Aspose.3D for Java ermöglicht die Aufdeckung der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mit der `evaluateGlobalTransform` Methode auswerten. Das folgende Code-Snippet zeigt, wie die geometrische Transformation verfügbar gemacht wird.

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
