---
title: Crea poligono in mesh
type: docs
weight: 40
url: /it/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET consente di creare un poligono in una mesh. Per utilizzare la funzionalità, API offre il metodo CreatePolygon della classe Mesh.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 
##  **Crea poligono in mesh**
Aspose.3D for Python via .NET consente di creare un poligono in una mesh. Per utilizzare la funzionalità, API offre il metodo [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) della classe [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Utilizzando il metodo `create_polygon` è possibile creare un poligono ottimizzato [Triangolo](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)o [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) senza allocare memoria extra. Il seguente frammento di codice mostra come utilizzare questa funzionalità.

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
