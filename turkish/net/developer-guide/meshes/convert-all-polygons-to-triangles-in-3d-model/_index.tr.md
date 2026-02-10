---
title: Tüm poligonları 3D modelinde üçgenlere dönüştürün
type: docs
weight: 50
url: /tr/net/convert-all-polygons-to-triangles-in-3d-model/
description: Using Aspose.3D for .NET API, developers can convert all polygons to triangles in any supported 3D file.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, developers can convert all polygons to triangles in any supported 3D file.

{{% /alert %}}
##  **Tonvert All olyolygons Triangles**
Bu kod örneğinde gösterildiği gibi bir parametre olarak [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıf nesnesini alan [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) sınıfında `Triangulate` yönteminin başka bir aşırı yüklenmesini ekledik:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
