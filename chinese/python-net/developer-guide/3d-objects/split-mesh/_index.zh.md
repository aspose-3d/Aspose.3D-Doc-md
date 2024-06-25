---
title: 分割网格
type: docs
weight: 100
url: /zh/python-net/split-mesh/
description: 开发人员可能需要将场景的所有网格拆分为每个材质的几个子网格。如果已为场景指定了单个材质，则SplitMesh方法不会拆分场景的网格。开发人员现在可以使用 Aspose.3D for Python via .NET API 来实现此目的。
---
##  **每个素材分割场景的所有网格**
开发人员可能需要将场景的所有网格拆分为每个材质的几个子网格。`split_mesh` 方法不会拆分场景的网格 (如果已为其指定了单个材质)。开发人员现在可以使用 [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API 来实现此目的。

{{% alert color="primary" %}}

`SplitMeshPolicy` enum指定网格拆分算法中使用的数据策略，它支持两种策略，在子网格之间共享数据或每个子网格都有自己的数据 (仅使用的数据)。

{{% /alert %}}

下面的代码示例按材质拆分场景的所有网格。每个子网格共享相同的直接数据，并且仅在索引上有所不同。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
##  **通过指定材质来分割网格**
Aspose.3D for Python via .NET API 允许开发人员通过手动指定材质来拆分网格。“分割网格” 选项创建单独的对象，每个子网格将仅使用一种材质。
###  **分割盒子的网格**
此帮助主题创建了框的网格，以保持代码的全面和简短。开发人员可以按照以下帮助主题中的说明手动构建网格: [创建 3D 立方体网格](/3d/zh/python-net/create-3d-mesh-and-scene/)。此外，一个盒子由6个平面组成，每个平面将成为一个子网格。下面的代码示例通过手动指定材质来拆分原始网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
