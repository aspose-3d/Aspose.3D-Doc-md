---
title: 简单多边形的三角剖分
type: docs
weight: 30
url: /zh/python-net/triangulation-of-a-simple-polygon/
description: 使用 Aspose.3D for Python via .NET API，开发人员可以对简单多边形进行三角测量。任何多边形都可以划分为三角形。三角形的所有操作和计算可以分段应用于多边形。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API，开发人员可以对简单多边形进行三角测量。任何多边形都可以划分为三角形。三角形的所有操作和计算可以分段应用于多边形。

{{% /alert %}}
##  **三角化多边形**
开发人员可能会从多边形区域中选取顶点，然后通过调用 [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) 类的三角化方法来形成三角形，每个三角形的形式为V{1}，V{i-1}，V{i}，索引i从3到n。演示应用程序 (名称: Triangulate) 下 `Triangulate/PolygonCanvas.py` 文件中的 `Vertex` 和 `PolygonCanvas` 类演示了使用 Aspose.3D API 对多边形进行三角剖分的方法。

{{% alert color="primary" %}}

我们准备了一个演示项目。请参阅 [这个网址](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos)。

{{% /alert %}}
###  **三角测量的编程示例**
此代码示例从多边形区域中拾取顶点，然后应用算法创建三角形。您可以从 [这里](https://github.com/aspose-3d/Aspose.3D-for-.NET/) 下载此示例的完整工作项目。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.py" >}}
