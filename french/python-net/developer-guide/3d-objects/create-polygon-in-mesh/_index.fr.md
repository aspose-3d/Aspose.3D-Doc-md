---
title: Créer un polygone dans le maillage
type: docs
weight: 40
url: /fr/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET permet de créer un polygone dans un maillage. Pour utiliser la fonctionnalité, API offre la méthode CreatePolygon de la classe Mesh.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 
##  **Créer un polygone dans le maillage**
Aspose.3D for Python via .NET permet de créer un polygone dans un maillage. Afin d'utiliser la fonctionnalité, API offre la méthode [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) de la classe [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). En utilisant la méthode `create_polygon`, vous pouvez créer un polygone [Triangle](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) ou [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) optimisé sans allouer de mémoire supplémentaire. L'extrait de code suivant montre comment utiliser cette fonctionnalité.

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
