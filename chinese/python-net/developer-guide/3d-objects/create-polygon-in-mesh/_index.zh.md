---
title: 在网格中创建多边形
type: docs
weight: 40
url: /zh/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET 允许在网格中创建多边形。为了使用该功能，API 提供了Mesh类的CreatePolygon方法。
---
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 
##  **在网格中创建多边形**
Aspose.3D for Python via .NET 允许在网格中创建多边形。为了使用该功能，API 提供了 [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) 类的 [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) 方法。使用 `create_polygon` 方法，您可以创建一个优化的 [三角形](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) 或 [四边形](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) 多边形，而无需分配额外的内存。下面的代码段演示如何使用此功能。

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
