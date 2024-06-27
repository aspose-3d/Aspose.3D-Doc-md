---
title: 为 3D 模型的所有网格生成正常数据
type: docs
weight: 40
url: /zh/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API 支持为 3D 模型的所有网格生成正常数据 (没有正常数据)。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持为 3D 模型的所有网格生成正常数据 (没有正常数据)。

{{% /alert %}} 
##  **为 3DS 模型的所有网格生成正常数据**
`PolygonModifier` 类公开的generateNormal方法可用于为 3DS 文件中的所有网格生成正常数据。如果在网格中定义了VertexElementSmoothingGroup元素，则生成的法线数据将由VertexElementSmoothingGroup平滑。
###  **编程示例**
此代码示例加载一个 3DS 文件，访问所有节点并为所有网格创建正常数据。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
