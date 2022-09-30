---
title: 简单多边形的三角剖分
type: docs
weight: 30
url: /zh/net/triangulation-of-a-simple-polygon/
description: 使用Aspose.3D for .NET API，开发人员可以对一个简单的多边形进行三角测量。任何多边形都可以分为三角形。三角形的所有运算和计算都可以分段应用于多边形。
---
{{% alert color="primary" %}}

使用[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API，开发人员可以对一个简单的多边形进行三角测量。任何多边形都可以分为三角形。三角形的所有运算和计算都可以分段应用于多边形。

{{% /alert %}}
## **三角化多边形**
开发人员可能会从多边形区域中选择顶点，然后通过调用[`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)类的`Triangulate`方法来形成三角形，每个形式为V{1}，V{i-1}，V{i}，索引i从3到n。演示应用程序下的`Triangulate/PolygonCanvas.cs`文件中的`Vertex`和`PolygonCanvas`类 (名称: Triangulate) 演示了使用Aspose.3D API对多边形进行三角测量的方法。

{{% alert color="primary" %}}

我们准备了一个演示项目。请参考[这个网址](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos)。

{{% /alert %}}
### **三角测量的编程示例**
此代码示例从多边形区域中选择顶点，然后应用算法创建三角形。您可以从以下位置下载本示例的完整工作项目[这里](https://github.com/aspose-3d/Aspose.3D-for-.NET/)。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.cs" >}}
