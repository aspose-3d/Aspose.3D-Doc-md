---
title: Convertir tous les polygones en triangles dans le modèle 3D
type: docs
weight: 50
url: /fr/net/convert-all-polygons-to-triangles-in-3d-model/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent convertir tous les polygones en triangles dans n'importe quel fichier 3D pris en charge.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, les développeurs peuvent convertir tous les polygones en triangles dans n'importe quel fichier 3D pris en charge.

{{% /alert %}}
##  **Convertir tous les polygones en Triangles**
Nous avons ajouté une autre surcharge de la méthode `Triangulate` dans la classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) qui prend un objet de classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) comme paramètre comme indiqué dans cet exemple de code:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
