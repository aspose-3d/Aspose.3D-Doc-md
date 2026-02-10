---
title: Exponera geometrisk omvandling
type: docs
weight: 50
url: /sv/java/expose-geometric-transformation/
description: Aspose.3D for Java tillåter exponering av geometrisk transformation av en 3D scen. Du kan utvärdera den globala transformationen med hjälp av evalueringGlobalTransform metod.
---
#  **Exponera geometrisk omvandling**
Aspose.3D for Java tillåter exponering av geometrisk transformation av en 3D scen. Du kan utvärdera den globala transformationen med `evaluateGlobalTransform`-metoden. Följande kodsnutt visar hur man exponerar den geometriska transformationen.

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
