---
title: Expose Geometric Transformation
type: docs
weight: 50
url: /java/expose-geometric-transformation/
description: Aspose.3D for Java allows exposing geometric transformation of a 3D scene. You can evaluate the global transformation using evaluateGlobalTransform method.
---

# **Expose Geometric Transformation**
Aspose.3D for Java allows exposing geometric transformation of a 3D scene. You can evaluate the global transformation using `evaluateGlobalTransform` method. The following code snippet shows how to expose the geometric transformation.

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
