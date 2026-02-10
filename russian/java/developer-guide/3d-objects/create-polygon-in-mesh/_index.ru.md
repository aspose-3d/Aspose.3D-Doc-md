---
title: Создать многоугольник в сетке
type: docs
weight: 80
url: /ru/java/create-polygon-in-mesh/
description: Aspose.3D for Java позволяет создать многоугольник в сетке.
---
##  **Создать многоугольник в сетке**
Aspose.3D for Java позволяет создать многоугольник в сетке. Чтобы использовать эту функциональность, API предлагает метод [Creategon](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) класса [Сетка](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). Используя метод CreatePolygon, вы можете создать оптимизированный полигон [Треугольник](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) или [Квад](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) без выделения дополнительной памяти. Следующий фрагмент кода показывает, как использовать эту функциональность.



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
