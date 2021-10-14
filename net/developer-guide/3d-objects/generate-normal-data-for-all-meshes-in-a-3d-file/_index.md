---
title: Generate Normal Data for All Meshes in a 3D File
type: docs
weight: 70
url: /net/generate-normal-data-for-all-meshes-in-a-3d-file/
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can generate normal data for all meshes in any 3D model (without the normal data).

{{% /alert %}}
## **Generate Normal Data for All Meshes in a 3DS File**
The GenerateNormal method exposed by the [PolygonModifier](http://www.aspose.com/api/net/3d/aspose.threed.entities/polygonmodifier) class can be used to generate normal data for all meshes in a 3DS file. If VertexElementSmoothingGroup element was defined in the mesh, the generated normal data will get smoothed by the VertexElementSmoothingGroup.
### **Programming Sample**
This code example loads a 3DS file, visit all nodes and create normal data for all meshes.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.cs" >}}
