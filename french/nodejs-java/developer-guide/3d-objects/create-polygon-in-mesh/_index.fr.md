---
title: Créer un polygone dans le maillage
type: docs
weight: 80
url: /fr/nodejs-java/create-polygon-in-mesh/
description: Aspose.3D for Node.js via Java permet de créer un polygone dans un maillage.
---
##  **Créer un polygone dans le maillage**
Aspose.3D for Node.js via Java permet de créer un polygone dans un maillage. Afin d'utiliser la fonctionnalité, API offre la méthode [CréerPolygone](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) de la classe [Maille](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). En utilisant la méthode CreatePolygon, vous pouvez créer un polygone [Triangle](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) ou [Quad](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) optimisé sans allouer de mémoire supplémentaire. L'extrait de code suivant montre comment utiliser cette fonctionnalité.



{{< highlight "java" >}}

// Initialize Mesh
var mesh = new aspose.threed.Mesh();

//The old CreatePolygon needs to create a temporary array for holding the face indices
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);

//Or You can create a polygon using 4 vertices(quad)
//mesh.createPolygon(0, 1, 2, 3);

{{< /highlight >}}
