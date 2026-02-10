---
title: Skapa polygon i mesh
type: docs
weight: 40
url: /sv/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET tillåter att skapa en polygon i en mesh. För att använda funktionaliteten erbjuder API CreatePolygon-metoden i Mesh-klass.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 
##  **Skapa polygon i mesh**
Aspose.3D for Python via .NET tillåter att skapa en polygon i en mesh. För att kunna använda funktionaliteten erbjuder API-metoden [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) för klassen [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Med `create_polygon`-metoden kan du skapa ett optimerat [Triangeln](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) eller [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)-polygon utan att tilldela extra minne. Följande kodsnutt visar hur denna funktionalitet används.

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
