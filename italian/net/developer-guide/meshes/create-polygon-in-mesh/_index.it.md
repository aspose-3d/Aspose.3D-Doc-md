---
title: Crea poligono in mesh
type: docs
weight: 14
url: /it/net/create-polygon-in-mesh/
description: Aspose.3D for .NET consente di creare un poligono in una mesh. Per utilizzare la funzionalità, API offre il metodo CreatePolygon della classe Mesh.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 
##  **Crea poligono in mesh**
Aspose.3D for .NET consente di creare un poligono in una mesh. Per utilizzare la funzionalità, API offre il metodo [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) della classe [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Utilizzando il metodo CreatePolygon è possibile creare un poligono ottimizzato [Triangolo](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)o [Quad](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) senza allocare memoria extra. Il seguente frammento di codice mostra come utilizzare questa funzionalità.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
