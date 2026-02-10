---
title: Erstellen Sie Polygon in der Masche
type: docs
weight: 80
url: /de/java/create-polygon-in-mesh/
description: Aspose.3D for Java ermöglicht das Erstellen eines Polygons in einem Netz.
---
##  **Erstellen Sie Polygon in der Masche**
Aspose.3D for Java ermöglicht das Erstellen eines Polygons in einem Netz. Um die Funktional ität nutzen zu können, bietet die API die [Create Polygon](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-)-Methode der [Netz](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh)-Klasse. Mit der CreatePolygon-Methode können Sie ein optimiertes [Dreieck](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-)-oder [Quad](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-)-Polygon erstellen, ohne zusätzlichen Speicher zuzuweisen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird.



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize Mesh
Mesh mesh = new Mesh();
//The old CreatePolygon needs to create a temporary array for holding the face indices
//mesh.createPolygon(new int[] { 0, 1, 2 });
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);
//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
