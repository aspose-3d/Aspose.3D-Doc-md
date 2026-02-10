---
title: Erstellen Sie Polygon in der Masche
type: docs
weight: 14
url: /de/net/create-polygon-in-mesh/
description: Aspose.3D for .NET ermöglicht das Erstellen eines Polygons in einem Netz. Um die Funktional ität nutzen zu können, bietet die API die CreatePolygon-Methode der Mesh-Klasse.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 
##  **Erstellen Sie Polygon in der Masche**
Aspose.3D for .NET ermöglicht das Erstellen eines Polygons in einem Netz. Um die Funktional ität nutzen zu können, bietet die API die [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)-Methode der [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh)-Klasse. Mit der CreatePolygon-Methode können Sie ein optimiertes [Dreieck](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)-oder [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)-Polygon erstellen, ohne zusätzlichen Speicher zuzuweisen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
