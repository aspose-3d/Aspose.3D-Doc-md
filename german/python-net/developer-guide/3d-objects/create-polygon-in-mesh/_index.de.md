---
title: Erstellen Sie Polygon in der Masche
type: docs
weight: 40
url: /de/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET ermöglicht das Erstellen eines Polygons in einem Netz. Um die Funktional ität nutzen zu können, bietet die API die CreatePolygon-Methode der Mesh-Klasse.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 
##  **Erstellen Sie Polygon in der Masche**
Aspose.3D for Python via .NET ermöglicht das Erstellen eines Polygons in einem Netz. Um die Funktional ität nutzen zu können, bietet die API die [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)-Methode der [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh)-Klasse. Mit der `create_polygon`-Methode können Sie ein optimiertes [Dreieck](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)-oder [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1)-Polygon erstellen, ohne zusätzlichen Speicher zuzuweisen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird.

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
