---
title: Split Mesh
type: docs
weight: 10
url: /java/split-mesh/
description: Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.
---

## **Split all Meshes of Scene Per Material**
Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum specifies the data policy used in mesh splitting algorithm, it supports two policies, share data between sub-meshes or each sub-mesh has its own data (only used data).

{{% /alert %}} 

The code sample below splits all meshes of a scene per material. Each sub mesh shares the same direct data and only differs in indices.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
## **Split a Mesh by Specifying the Material**
Aspose.3D for Java API has support to split a mesh by manually specifying the material. The split mesh option creates separate objects and each sub mesh will use only one material.
### **Split Mesh of Box**
This help topic creates a mesh of the box to keep the code comprehensive and short. Developers may construct a mesh manually as narrated in this help topic: [Create a 3D Cube Mesh](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Furthermore, a box is composed by 6 planes and each plane will become a sub mesh. The code sample below splits a primitive mesh by manually specifying material.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
