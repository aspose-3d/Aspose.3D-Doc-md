---
title: 分割网格
type: docs
weight: 10
url: /zh/java/split-mesh/
description: Aspose.3D for Java API 支持将场景的所有网格拆分为每个材质的多个子网格。SplitMesh方法不会拆分场景的网格 (如果已为其指定了单个材质)。可以使用 Aspose.3D for Java API 来实现。
---
##  **分割每个材料的所有场景网格**
Aspose.3D for Java API 支持将场景的所有网格拆分为每个材质的多个子网格。SplitMesh方法不会拆分场景的网格 (如果已为其指定了单个材质)。可以使用 Aspose.3D for Java API 来实现。

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum指定网格拆分算法中使用的数据策略，它支持两种策略，在子网格之间共享数据或每个子网格都有自己的数据 (仅使用的数据)。

{{% /alert %}} 

下面的代码示例按材质拆分场景的所有网格。每个子网格共享相同的直接数据，并且仅在索引上有所不同。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
##  **通过指定材质来分割网格**
Aspose.3D for Java API 支持通过手动指定材质来拆分网格。“分割网格” 选项创建单独的对象，每个子网格将仅使用一种材质。
###  **盒子的分割网格**
此帮助主题创建了框的网格，以保持代码的全面和简短。开发人员可以按照以下帮助主题中的说明手动构建网格: [创建 3D 立方体网格](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene)。此外，一个盒子由6个平面组成，每个平面将成为一个子网格。下面的代码示例通过手动指定材质来拆分原始网格。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
