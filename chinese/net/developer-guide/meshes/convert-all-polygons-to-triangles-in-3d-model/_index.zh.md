---
title: 将 3D 模型中的所有多边形转换为三角形
type: docs
weight: 50
url: /zh/net/convert-all-polygons-to-triangles-in-3d-model/
description: 使用 Aspose.3D for .NET API，开发人员可以在任何受支持的 3D 文件中将所有多边形转换为三角形。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](http://products.aspose.com/3d/net) API，开发人员可以在任何受支持的 3D 文件中将所有多边形转换为三角形。

{{% /alert %}}
##  **将所有多边形转换为三角形**
我们在 [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) 类中添加了另一个 `Triangulate` 方法的重载，它将 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类对象作为参数，如下面的代码示例所示:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
