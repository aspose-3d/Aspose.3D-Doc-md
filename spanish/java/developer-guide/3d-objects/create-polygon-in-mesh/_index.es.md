---
title: Crear polígono en malla
type: docs
weight: 80
url: /es/java/create-polygon-in-mesh/
description: Aspose.3D for Java permite crear un polígono en una malla.
---
##  **Crear polígono en malla**
Aspose.3D for Java permite crear un polígono en una malla. Para usar la funcionalidad, el API ofrece el método [CreatePolígono](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) de la clase [Malla](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). Usando el método CreatePolygon puede crear un polígono [Triángulo](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-)o [Cuádruple](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) optimizado sin asignar memoria adicional. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad.



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
