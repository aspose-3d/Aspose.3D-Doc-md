---
title: 添加节点层次结构并在3D场景的多个节点之间共享网格的几何数据
type: docs
weight: 40
url: /zh/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D Python via .NET提供构建节点层次结构。节点是场景的基本构建块。节点的层次结构定义了场景的逻辑结构，并通过将几何图形，灯光和摄像机附加到节点来提供可见的内容。
---
## **在3D场景文档中添加节点层次结构**
Aspose.3D Python via .NET提供构建节点层次结构。节点是场景的基本构建块。节点的层次结构定义了场景的逻辑结构，并通过将几何图形，灯光和摄像机附加到节点来提供可见的内容。
### **场景图示例**
一个示例场景层次结构看起来像:

![todo: 图像_alt_文本](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

在Aspose.3D中，每个`Node`实例可以具有多个子节点，在本示例中，我们创建了一个具有两个多维数据集节点的节点，如果我们旋转根节点，则所有子节点也会受到影响:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
## **在多个节点之间共享网格的几何数据**
为了减少内存的必要性，可以将[`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh)类的单个实例绑定到[`Node`](https://reference.aspose.com/3d/net/aspose.threed/node)类的各种实例。设想您需要一个系统，其中所有3D立方体似乎都是无法区分的，但是您需要大量的它们。当系统启动时，您可以通过制作一个网格对象来节省内存。此时，每次需要另一个形状时，都要制作另一个节点对象，然后将该节点指向一个网格。这叫做实例化。Aspose.3D Python via .NET api允许进行实例化。
### **实例化示例**
在RTS (实时策略) 游戏中，我们总是可以看到具有相同3D模型的多个npc (非玩家角色)，也许颜色不同，渲染引擎通常在不同的npc上共享相同的网格几何数据，这种技术称为实例化。

{{% alert color="primary" %}}

代码中使用了`Mesh`类对象。我们可以[创建一个`Mesh`类对象，如在那里叙述](/3d/zh/python-net/create-3d-mesh-and-scene/)。

{{% /alert %}}

演示示例代码:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

在此示例中，我们创建了3个多维数据集节点共享相同的网格，每个节点具有不同的材质和不同的颜色。
