---
title: Создать многоугольник в сетке
type: docs
weight: 80
url: /ru/nodejs-java/create-polygon-in-mesh/
description: Aspose.3D for Node.js via Java позволяет создать многоугольник в сетке.
---
##  **Создать многоугольник в сетке**
Aspose.3D for Node.js via Java позволяет создать многоугольник в сетке. Чтобы использовать функциональность, API предлагает метод [Creategon](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) класса [Сетка](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). Используя метод CreatePolygon, вы можете создать оптимизированный полигон [Треугольник](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) или [Квад](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) без выделения дополнительной памяти. Следующий фрагмент кода показывает, как использовать эту функциональность.



{{< highlight "java" >}}

// Initialize Mesh
var mesh = new aspose.threed.Mesh();

//The old CreatePolygon needs to create a temporary array for holding the face indices
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);

//Or You can create a polygon using 4 vertices(quad)
//mesh.createPolygon(0, 1, 2, 3);

{{< /highlight >}}
