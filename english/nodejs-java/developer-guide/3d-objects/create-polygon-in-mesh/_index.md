---
title: Create Polygon In Mesh
type: docs
weight: 80
url: /nodejs-java/create-polygon-in-mesh/
description: Aspose.3D for Node.js via Java allows creating a polygon in a mesh.
---

## **Create Polygon In Mesh**
Aspose.3D for Node.js via Java allows creating a polygon in a mesh. In order to use the functionality, the API offers [createPolygon](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) method of [Mesh ](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh)class. Using CreatePolygon method you can create an optimized [Triangle ](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-)or [Quad ](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-)polygon without allocating extra memory. The following code snippet shows how to use this functionality. 



{{< highlight java >}}

// Initialize Mesh
var mesh = new aspose.threed.Mesh();

//The old CreatePolygon needs to create a temporary array for holding the face indices
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);

//Or You can create a polygon using 4 vertices(quad)
//mesh.createPolygon(0, 1, 2, 3);

{{< /highlight >}}
