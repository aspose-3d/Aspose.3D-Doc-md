---
title: Esponi la trasformazione geometrica
type: docs
weight: 50
url: /it/java/expose-geometric-transformation/
description: Aspose.3D for Java consente di esporre la trasformazione geometrica di una scena di 3D. È possibile valutare la trasformazione globale utilizzando il metodo evalGlobalTransform.
---
#  **Esponi la trasformazione geometrica**
Aspose.3D for Java consente di esporre la trasformazione geometrica di una scena di 3D. Puoi valutare la trasformazione globale usando il metodo `evaluateGlobalTransform`. Il seguente frammento di codice mostra come esporre la trasformazione geometrica.

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
