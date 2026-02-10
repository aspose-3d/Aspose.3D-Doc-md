---
title: Create Polygon In Mesh
type: docs
weight: 14
url: /net/create-polygon-in-mesh/
description: Aspose.3D for .NET allows creating a polygon in a mesh. In order to use the functionality, the API offers CreatePolygon method of Mesh class. 
---

{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 
## **Create Polygon In Mesh**
Aspose.3D for .NET allows creating a polygon in a mesh. In order to use the functionality, the API offers [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) method of [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) class. Using CreatePolygon method you can create an optimized [Triangle ](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)or [Quad ](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)polygon without allocating extra memory. The following code snippet shows how to use this functionality. 

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
