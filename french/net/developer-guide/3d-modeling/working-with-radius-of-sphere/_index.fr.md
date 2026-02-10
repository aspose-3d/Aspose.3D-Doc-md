---
title: Travailler avec le rayon de la sphère
type: docs
weight: 110
url: /fr/net/working-with-radius-of-sphere/
description: En utilisant Aspose.3D for .NET, vous pouvez définir le rayon de get d'une sphère. Pour obtenir ou définir un rayon, vous pouvez utiliser la propriété Radius de la classe Sphere. Voici l'exemple de code pour définir le rayon d'une sphère.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.4 ou supérieure.

{{% /alert %}} 
##  **Travail avec rayon de sphère**
En utilisant Aspose.3D for .NET, vous pouvez définir le rayon de get d'une sphère. Pour obtenir ou définir un rayon, vous pouvez utiliser la propriété `Radius` de la classe `Sphere`. Voici l'exemple de code pour définir le rayon d'une sphère.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
