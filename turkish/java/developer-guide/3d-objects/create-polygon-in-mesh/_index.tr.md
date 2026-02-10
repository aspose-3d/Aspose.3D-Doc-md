---
title: Create olyolygon In Mesh
type: docs
weight: 80
url: /tr/java/create-polygon-in-mesh/
description: Aspose.3D for Java bir ağda bir çokgen oluşturmaya izin verir.
---
##  **Create olyolygon In Mesh**
Aspose.3D for Java allows creating a polygon in a mesh. In order to use the functionality, the API offers [createPolygon](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) method of [Mesh ](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh)class. Using CreatePolygon method you can create an optimized [Triangle ](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-)or [Quad ](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-)polygon without allocating extra memory. The following code snippet shows how to use this functionality. 



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
