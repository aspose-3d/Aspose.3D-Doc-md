---
title: 分割网格
type: docs
weight: 100
url: /zh/python-net/split-mesh/
description: 开发人员可能需要将场景的所有网格拆分为每个材料的几个子网格。如果已为场景分配了单个材质，则SplitMesh方法将不会分割场景的网格。开发人员现在可以通过使用Aspose.3D进行Python via .NET API来实现这一点。
---
## **每个素材分割场景的所有网格**
开发人员可能需要将场景的所有网格拆分为每个材料的几个子网格。如果`split_mesh`方法已分配了单个材料，则不会分割场景的网格。开发人员现在可以通过使用[Aspose.3D为Python via .NET](https://products.aspose.com/3d/python-net/)API。

{{% alert color="primary" %}}

`SplitMeshPolicy`枚举指定网格分割算法中使用的数据策略，它支持两个策略，在子网格之间共享数据或每个子网格都有自己的数据 (仅使用的数据)。

{{% /alert %}}

下面的代码示例按材质拆分场景的所有网格。每个子网格共享相同的直接数据，并且仅在索引上有所不同。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
## **通过指定材质来分割网格**
Python via .NET API的Aspose.3D允许开发人员通过手动指定材质来分割网格。分割网格选项创建单独的对象，每个子网格将仅使用一种材质。
### **分割盒子的网格**
此帮助主题创建框的网格，以保持代码的全面和简短。开发人员可以按照本帮助主题中的叙述手动构造网格:[创建3D立方体网格](/3d/zh/python-net/create-3d-mesh-and-scene/)。此外，一个盒子由6个平面组成，每个平面将成为一个子网格。下面的代码示例通过手动指定材质来拆分原始网格。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
