---
title: 为 3D 文件中的所有网格生成普通数据
type: docs
weight: 17
url: /zh/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: 使用 Aspose.3D for .NET，开发人员可以为任何 3D 模型中的所有网格生成正常数据 (没有正常数据)。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员可以为任何 3D 模型中的所有网格生成正常数据 (没有正常数据)。

{{% /alert %}}
##  **为 3DS 文件中的所有网格生成普通数据**
由 [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) 类公开的 `GenerateNormal` 方法可用于为 3DS 文件中的所有网格生成普通数据。如果在网格中定义了 `VertexElementSmoothingGroup` 元素，则生成的法线数据将被 `VertexElementSmoothingGroup` 平滑。
###  **编程示例**
此代码示例加载一个 3DS 文件，访问所有节点并为所有网格创建正常数据。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.cs" >}}
