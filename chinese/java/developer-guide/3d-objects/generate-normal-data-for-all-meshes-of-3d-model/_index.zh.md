---
title: 为3D模型的所有网格生成正常数据
type: docs
weight: 40
url: /zh/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API支持为3D模型的所有网格生成正常数据 (没有正常数据)。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API支持为3D模型的所有网格生成正常数据 (没有正常数据)。

{{% /alert %}} 
## **为3DS模型的所有网格生成正常数据**
`PolygonModifier`类公开的generateNormal方法可用于为3DS文件中的所有网格生成正常数据。如果在网格中定义了VertexElementSmoothingGroup元素，则生成的正常数据将由VertexElementSmoothingGroup进行平滑处理。
### **编程示例**
此代码示例加载3DS文件，访问所有节点并为所有网格创建正常数据。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
