---
title: Split Mesh
type: docs
weight: 100
url: /python-net/split-mesh/
description: Developers may require to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene If it has been assigned a single material. Developers can now achieve this by using Aspose.3D for Python via .NET API.
---

## **Split All Meshes of a Scene Per Material**
Developers may require to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene If it has been assigned a single material. Developers can now achieve this by using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

SplitMeshPolicy enum specifies the data policy used in mesh splitting algorithm, it supports two policies, share data between sub-meshes or each sub-mesh has its own data (only used data).

{{% /alert %}}

The code sample below splits all meshes of a scene per material. Each sub mesh shares the same direct data and only differs in indices.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
## **Split a Mesh by Specifying the Material**
Aspose.3D for Python via .NET API allows developers to split a mesh by manually specifying the material. The split mesh option creates separate objects and each sub mesh will use only one material.
### **Split the Mesh of Box**
This help topic creates a mesh of the box to keep the code comprehensive and short. Developers may construct a mesh manually as narrated in this help topic: [Create a 3D Cube Mesh](/3d/python-net/create-3d-mesh-and-scene/). Furthermore, a box is composed by 6 planes and each plane will become a sub mesh. The code sample below splits a primitive mesh by manually specifying the material.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
