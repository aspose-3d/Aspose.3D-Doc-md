---
title: Convertir todos los polígonos a triángulos en el modelo 3D
type: docs
weight: 50
url: /es/net/convert-all-polygons-to-triangles-in-3d-model/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden convertir todos los polígonos en triángulos en cualquier archivo 3D compatible.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, los desarrolladores pueden convertir todos los polígonos en triángulos en cualquier archivo 3D compatible.

{{% /alert %}}
##  **Convertir todos los polígonos a triángulos**
Hemos agregado otra sobrecarga del método `Triangulate` en la clase [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) que toma un objeto de clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) como parámetro como se muestra en este ejemplo de código:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
