---
title : "Split Mesh" 
description : "" 
weight : 12044 
toc : false
type: docs
url: /java/developerguide/mesh/split+mesh/
---

# Aspose.3D for Java : Split Mesh


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Split all Meshes of Scene Per Material](#split-all-meshes-of-scene-per-material)
*   2 [Split a Mesh by Specifying the Material](#split-a-mesh-by-specifying-the-material)
    *   2.1 [Split Mesh of Box](#split-mesh-of-box)
{{< /panel >}}
 

 

## Split all Meshes of Scene Per Material

Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The `SplitMesh` method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.

`SplitMeshPolicy` enum specifies the data policy used in mesh splitting algorithm, it supports two policies, share data between sub-meshes or each sub-mesh has its own data (only used data).

The code sample below splits all meshes of a scene per material. Each sub mesh shares the same direct data and only differs in indices.

## Split a Mesh by Specifying the Material

Aspose.3D for Java API has support to split a mesh by manually specifying the material. The split mesh option creates separate objects and each sub mesh will use only one material.

### Split Mesh of Box

This help topic creates a mesh of the box to keep the code comprehensive and short. Developers may construct a mesh manually as narrated in this help topic: [Create a 3D Cube Mesh](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Furthermore, a box is composed by 6 planes and each plane will become a sub mesh. The code sample below splits a primitive mesh by manually specifying material.

