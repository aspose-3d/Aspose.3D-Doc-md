---
title: Créer un polygone dans le maillage
type: docs
weight: 14
url: /fr/net/create-polygon-in-mesh/
description: Aspose.3D for .NET permet de créer un polygone dans un maillage. Pour utiliser la fonctionnalité, le API offre la méthode CreatePolygon de la classe Mesh.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 
##  **Créer un polygone dans le maillage**
Aspose.3D for .NET permet de créer un polygone dans un maillage. Pour utiliser la fonctionnalité, API propose la méthode [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) de la classe [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). En utilisant la méthode CreatePolygon, vous pouvez créer un polygone [Triangle](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) ou [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) optimisé sans allouer de mémoire supplémentaire. L'extrait de code suivant montre comment utiliser cette fonctionnalité.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
