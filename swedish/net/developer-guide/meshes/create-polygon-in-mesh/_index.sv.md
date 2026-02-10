---
title: Skapa polygon i mesh
type: docs
weight: 14
url: /sv/net/create-polygon-in-mesh/
description: Aspose.3D for .NET tillåter att en polygon skapas i ett mesh. För att använda funktionaliteten erbjuder API CreatePolygon-metoden i Mesh-klass.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 
##  **Skapa polygon i mesh**
Aspose.3D for .NET tillåter att en polygon skapas i ett mesh. För att kunna använda funktionaliteten erbjuder API-metoden [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) för klassen [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Genom att använda CreatePolygon-metoden kan du skapa ett optimerat [Triangeln](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) eller [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)polygon utan att tilldela extra minne. Följande kodsnutt visar hur denna funktionalitet används.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
