---
title: Создать многоугольник в сетке
type: docs
weight: 14
url: /ru/net/create-polygon-in-mesh/
description: Aspose.3D for .NET позволяет создать многоугольник в сетке. Для того, чтобы использовать функциональность, API предлагает метод CreatePolygon класса Mesh.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 
##  **Создать многоугольник в сетке**
Aspose.3D for .NET позволяет создать многоугольник в сетке. Чтобы использовать эту функциональность, API предлагает метод [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) класса [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Используя метод CreatePolygon, вы можете создать оптимизированный полигон [Треугольник](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) или [Квад](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) без выделения дополнительной памяти. Следующий фрагмент кода показывает, как использовать эту функциональность.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
