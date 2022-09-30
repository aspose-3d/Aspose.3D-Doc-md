---
title: 为3D文件中的所有网格生成正常数据
type: docs
weight: 70
url: /zh/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: 使用Aspose.3D进行Python via .NET，开发人员可以为任何3D模型中的所有网格生成正常数据 (没有正常数据)。
---
{{% alert color="primary" %}}

使用[Aspose.3D为Python via .NET](https://products.aspose.com/3d/python-net/),开发人员可以为任何3D模型中的所有网格生成正常数据 (没有正常数据)。

{{% /alert %}}
## **为3DS文件中的所有网格生成正常数据**
[`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)类公开的`generate_normal`方法可用于为3DS文件中的所有网格生成正常数据。如果在网格中定义了`VertexElementSmoothingGroup`元素，则生成的正常数据将被`VertexElementSmoothingGroup`平滑。
### **编程示例**
此代码示例加载3DS文件，访问所有节点并为所有网格创建正常数据。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
