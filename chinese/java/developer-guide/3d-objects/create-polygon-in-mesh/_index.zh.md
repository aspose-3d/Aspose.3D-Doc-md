---
title: 在网格中创建多边形
type: docs
weight: 80
url: /zh/java/create-polygon-in-mesh/
description: Aspose.3D for Java 允许在网格中创建多边形。
---
##  **在网格中创建多边形**
Aspose.3D for Java 允许在网格中创建多边形。为了使用该功能，API 提供了 [网格](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh) 类的 [创建多边形](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) 方法。使用CreatePolygon方法，您可以创建优化的 [三角形](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) 或 [四边形](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) 多边形，而无需分配额外的内存。下面的代码段演示如何使用此功能。



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
