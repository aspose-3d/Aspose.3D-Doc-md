---
title: Crea poligono in mesh
type: docs
weight: 80
url: /it/java/create-polygon-in-mesh/
description: Aspose.3D for Java consente di creare un poligono in una mesh.
---
##  **Crea poligono in mesh**
Aspose.3D for Java consente di creare un poligono in una mesh. Per utilizzare la funzionalità, API offre il metodo [CreatePoligono](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) della classe [Mesh](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). Utilizzando il metodo CreatePolygon è possibile creare un poligono ottimizzato [Triangolo](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-)o [Quad](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) senza allocare memoria extra. Il seguente frammento di codice mostra come utilizzare questa funzionalità.



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize Mesh
Mesh mesh = new Mesh();
//The old CreatePolygon needs to create a temporary array for holding the face indices
//mesh.createPolygon(new int[] { 0, 1, 2 });
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);
//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
