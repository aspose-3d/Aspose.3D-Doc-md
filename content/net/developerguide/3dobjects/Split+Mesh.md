+++
title = "Split Mesh" 
description = "" 
weight = 12048 
+++

Aspose.3D for .NET : Split Mesh  

# Aspose.3D for .NET : Split Mesh


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Split All Meshes of a Scene Per Material](#SplitMesh-SplitAllMeshesofaScenePerMaterial)
*   2 [Split a Mesh by Specifying the Material](#SplitMesh-SplitaMeshbySpecifyingtheMaterial)
    *   2.1 [Split the Mesh of Box](#SplitMesh-SplittheMeshofBox)
{{< /panel >}}
 

 

## Split All Meshes of a Scene Per Material

Developers may require to split all meshes of a scene into several sub meshes per material. The `SplitMesh` method will not split a mesh of the scene If it has been assigned a single material. Developers can now achieve this by using [Aspose.3D for .NET](http://www.aspose.com/3d-component-suite.aspx) API.

`SplitMeshPolicy` enum specifies the data policy used in mesh splitting algorithm, it supports two policies, share data between sub-meshes or each sub-mesh has its own data (only used data).

The code sample below splits all meshes of a scene per material. Each sub mesh shares the same direct data and only differs in indices.

## Split a Mesh by Specifying the Material

[Aspose.3D for .NET](http://www.aspose.com/3d-component-suite.aspx) API allows developers to split a mesh by manually specifying the material. The split mesh option creates separate objects and each sub mesh will use only one material.

### Split the Mesh of Box

This help topic creates a mesh of the box to keep the code comprehensive and short. Developers may construct a mesh manually as narrated in this help topic: [Create a 3D Cube Mesh](https://docs2.aspose.com/3d/net/developerguide/geometry/create+3d+mesh+and+scene). Furthermore, a box is composed by 6 planes and each plane will become a sub mesh. The code sample below splits a primitive mesh by manually specifying the material.

