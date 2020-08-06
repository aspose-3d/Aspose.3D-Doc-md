---
title: Generate Normal Data for All Meshes of 3D Model
type: docs
weight: 40
url: /java/generate-normal-data-for-all-meshes-of-3d-model/
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support of generating normal data for all meshes of 3D model (without the normal data).

{{% /alert %}} 
## **Generate Normal Data for All Meshes of 3DS Model**
The generateNormal method exposed by the **PolygonModifier** class can be used to generate normal data for all meshes in a 3DS file. If VertexElementSmoothingGroup element was defined in the mesh, the generated normal data will get smoothed by the VertexElementSmoothingGroup.
### **Programming Sample**
This code example loads a 3DS file, visit all nodes and create normal data for all meshes.

{{< gist "aspose-3d" "a10c42b56128eaadb7d7f81e2176306c" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
