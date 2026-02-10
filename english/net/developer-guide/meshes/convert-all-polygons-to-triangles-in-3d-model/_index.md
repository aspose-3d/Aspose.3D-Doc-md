---
title: Convert all Polygons to Triangles in 3D Model
type: docs
weight: 50
url: /net/convert-all-polygons-to-triangles-in-3d-model/
description: Using Aspose.3D for .NET API, developers can convert all polygons to triangles in any supported 3D file.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, developers can convert all polygons to triangles in any supported 3D file.

{{% /alert %}}
## **Convert All Polygons to Triangles**
We have added another overload of `Triangulate` method in the [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) class which takes a [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class object as a parameter as shown in this code example:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
