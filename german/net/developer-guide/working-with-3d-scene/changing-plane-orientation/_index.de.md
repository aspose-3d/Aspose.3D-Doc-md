---
title: Veränderung der Flugzeug orientierung
type: docs
weight: 40
url: /de/net/changing-plane-orientation/
description: Aspose.3D for .NET ermöglicht eine veränderte Ausrichtung einer Szene. Um die Ausrichtung zu ändern, wird die Up-Vektor-Eigenschaft in der Flugzeug klasse eingeführt.
---
##  **Veränderung der Flugzeug orientierung**
Aspose.3D for .NET ermöglicht eine veränderte Ausrichtung einer Szene. Um die Ausrichtung zu ändern, wird die `Up`-Vektor eigenschaft in der `Plane`-Klasse eingeführt. Das folgende Code-Snippet zeigt, wie die Ausrichtung des Flugzeugs geändert wird:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
