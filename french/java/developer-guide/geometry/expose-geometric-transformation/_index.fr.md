---
title: Exposer la transformation géométrique
type: docs
weight: 50
url: /fr/java/expose-geometric-transformation/
description: Aspose.3D for Java permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale à l'aide de la méthode evaluateGlobalTransform.
---
#  **Exposer la transformation géométrique**
Aspose.3D for Java permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale en utilisant la méthode `evaluateGlobalTransform`. L'extrait de code suivant montre comment exposer la transformation géométrique.

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
