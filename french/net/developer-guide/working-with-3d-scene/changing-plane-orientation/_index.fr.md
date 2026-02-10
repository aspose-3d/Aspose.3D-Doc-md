---
title: Changer l'orientation de l'avion
type: docs
weight: 40
url: /fr/net/changing-plane-orientation/
description: Aspose.3D for .NET permet de changer l'orientation d'une scène. Pour modifier l'orientation, la propriété de vecteur Up est introduite dans Plane Class.
---
##  **Changer l'orientation de l'avion**
Aspose.3D for .NET permet de changer l'orientation d'une scène. Pour changer l'orientation, la propriété de vecteur `Up` est introduite dans la classe `Plane`. L'extrait de code suivant montre comment modifier l'orientation du plan:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
