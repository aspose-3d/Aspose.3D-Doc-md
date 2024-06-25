---
title: Skapa polygon i mesh
type: docs
weight: 80
url: /sv/nodejs-java/create-polygon-in-mesh/
description: Aspose.3D for Node.js via Java tillåter att skapa en polygon i en mesh.
---
##  **Skapa polygon i mesh**
Aspose.3D for Node.js via Java tillåter att skapa en polygon i en mesh. För att kunna använda funktionaliteten erbjuder API-metoden [CreatePolygonName](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) för [Maska](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh)-klass. Genom att använda CreatePolygon-metoden kan du skapa ett optimerat [Triangeln](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) eller [Quad](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-)polygon utan att tilldela extra minne. Följande kodsnutt visar hur denna funktionalitet används.



{{< highlight "java" >}}

// Initialize Mesh
var mesh = new aspose.threed.Mesh();

//The old CreatePolygon needs to create a temporary array for holding the face indices
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);

//Or You can create a polygon using 4 vertices(quad)
//mesh.createPolygon(0, 1, 2, 3);

{{< /highlight >}}
