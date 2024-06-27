---
title: 添加节点层次结构并在 3D 场景的多个节点之间共享网格的几何数据
type: docs
weight: 40
url: /zh/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET 提供构建节点层次结构。节点是场景的基本构建块。节点层次结构定义场景的逻辑结构，并通过将几何图形、灯光和摄影机附加到节点来提供可见内容。
---
##  **在 3D 场景文档中添加节点层次结构**
Aspose.3D for .NET 提供构建节点层次结构。节点是场景的基本构建块。节点层次结构定义场景的逻辑结构，并通过将几何图形、灯光和摄影机附加到节点来提供可见内容。
###  **场景图示例**
一个示例场景层次结构看起来像:

![todo: 图像 _ alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

在 Aspose.3D 中，每个 `Node` 实例可以有多个子节点，在这个例子中，我们创建了一个有两个立方体节点的节点，如果我们旋转根节点，所有子节点也会受到影响:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.cs" >}}
##  **在多个节点之间共享网格的几何数据**
为了减少内存需求，可以将 [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) 类的单个实例绑定到 [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) 类的各个实例。设想您需要一个系统，其中所有 3D 立方体似乎都无法区分，但是您需要大量的立方体。您可以通过在系统开始时制作一个网格对象来节省内存。此时，每次需要另一个形状时，都要创建另一个节点对象，然后将该节点指向一个网格。这称为实例化。Aspose.3D for .NET api允许执行实例化。
###  **实例化示例**
在RTS (实时策略) 游戏中，我们总是可以看到多个npc (非玩家角色) 具有相同的 3D 模型，可能是不同的颜色，渲染引擎通常在不同的npc之间共享相同的网格几何数据，这种技术称为实例化。

{{% alert color="primary" %}}

代码中正在使用 `Mesh` 类对象。我们可以 [创建一个网格类对象，如在那里叙述](/3d/zh/net/create-3d-mesh-and-scene/)。

{{% /alert %}}

演示示例代码:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.cs" >}}

在此示例中，我们创建了3个多维数据集节点共享相同的网格，每个节点具有不同的材质和不同的颜色。
