---
title: Create olyolygon In Mesh
type: docs
weight: 14
url: /tr/net/create-polygon-in-mesh/
description: Aspose.3D for .NET bir ağda bir çokgen oluşturmaya izin verir. Işlevselliği kullanmak için, API, mesh sınıfının createpolygon yöntemini sunar.
---
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
##  **Create olyolygon In Mesh**
Aspose.3D for .NET allows creating a polygon in a mesh. In order to use the functionality, the API offers [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) method of [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) class. Using CreatePolygon method you can create an optimized [Triangle ](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)or [Quad ](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)polygon without allocating extra memory. The following code snippet shows how to use this functionality. 

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
