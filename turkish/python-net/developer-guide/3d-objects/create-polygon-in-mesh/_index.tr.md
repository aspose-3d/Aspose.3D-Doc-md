---
title: Create olyolygon In Mesh
type: docs
weight: 40
url: /tr/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET bir ağda bir çokgen oluşturmaya izin verir. Işlevselliği kullanmak için, API, mesh sınıfının createpolygon yöntemini sunar.
---
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
##  **Create olyolygon In Mesh**
Aspose.3D for Python via .NET allows creating a polygon in a mesh. In order to use the functionality, the API offers [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) method of [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) class. Using `create_polygon` method you can create an optimized [Triangle ](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)or [Quad ](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)polygon without allocating extra memory. The following code snippet shows how to use this functionality. 

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
