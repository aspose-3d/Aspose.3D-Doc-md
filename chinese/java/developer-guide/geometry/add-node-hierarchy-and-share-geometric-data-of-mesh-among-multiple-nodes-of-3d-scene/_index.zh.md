---
title: 添加节点层次结构并在3D场景的多个节点之间共享网格的几何数据
type: docs
weight: 20
url: /zh/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java支持构建节点的层次结构。节点是3D场景的基本构建块，节点的层次结构定义了3D场景的逻辑结构，并通过将几何图形、灯光和摄像机附加到节点来提供可见内容。
---
## **在3D场景文档中添加节点层次结构**
Aspose.3D for Java支持构建节点的层次结构。`Node`是3D场景的基本构建块，节点的层次结构定义3D场景的逻辑结构，并通过将几何图形、灯光和摄像机附加到节点来提供可见内容。
### **场景图示例**

在Aspose.3D中，每个`Node`实例可以具有多个子节点，在本示例中，我们创建了一个具有两个多维数据集节点的节点，如果我们旋转根节点，则所有子节点也会受到影响:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **在多个节点之间共享网格的几何数据**
为了减少内存的必要性，`Mesh`类的单个实例可以绑定到`Node`类的各种实例。设想您需要一个系统，其中所有3D立方体似乎都是无法区分的，但是您需要大量的它们。当系统启动时，您可以通过制作一个网格对象来节省内存。此时，每次需要另一个形状时，您都会创建另一个节点对象，然后将该节点指向一个`Mesh`。这叫做实例化。Aspose.3D for Java api允许进行实例化。
### **实例化示例**
在RTS (实时策略) 游戏中，我们总是可以看到具有相同3D模型的多个npc (非玩家角色)，也许颜色不同，渲染引擎通常在不同的npc上共享相同的网格几何数据，这种技术称为实例化。

{{% alert color="primary" %}} 

代码中使用了`Mesh`类对象。我们可以[创建一个网格类对象，如在那里叙述](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene)。

{{% /alert %}} 

演示示例代码:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


在此示例中，我们创建了3个多维数据集节点共享相同的网格，每个节点具有不同的材质和不同的颜色。
