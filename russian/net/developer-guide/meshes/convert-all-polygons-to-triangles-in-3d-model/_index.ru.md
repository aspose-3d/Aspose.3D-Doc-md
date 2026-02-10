---
title: Преобразовать все многоугольники в треугольники в модели 3D
type: docs
weight: 50
url: /ru/net/convert-all-polygons-to-triangles-in-3d-model/
description: Используя Aspose.3D for .NET API, разработчики могут конвертировать все многоугольники в треугольники в любом поддерживаемым 3D файле.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, разработчики могут конвертировать все многоугольники в треугольники в любом поддерживаемым файле 3D.

{{% /alert %}}
##  **Конвертировать Все полигоны в треугольники**
Мы добавили еще одну перегрузку метода `Triangulate` в класс [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), который принимает объект класса [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) в качестве параметра, как показано в этом примере кода:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
