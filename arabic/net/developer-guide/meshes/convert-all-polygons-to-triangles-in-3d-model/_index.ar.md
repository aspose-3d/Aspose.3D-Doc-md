---
title: تحويل جميع المضلعات إلى مثلثات في نموذج 3D
type: docs
weight: 50
url: /ar/net/convert-all-polygons-to-triangles-in-3d-model/
description: باستخدام Aspose.3D for .NET API ، يمكن للمطورين تحويل جميع المضلعات إلى مثلثات في أي ملف 3D مدعوم.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, developers can convert all polygons to triangles in any supported 3D file.

{{% /alert %}}
##  **Olyonvert ll ll olyأوليغونز إلى riri**
لقد أضفنا زيادة كبيرة أخرى على طريقة `Triangulate` في فئة [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) والتي تأخذ كائن فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) كمعلمة كما هو موضح في مثال الرمز هذا:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
