---
title: تحويل جميع المضلعات إلى مثلثات في نموذج 3D
type: docs
weight: 10
url: /ar/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: Using Aspose.3D for Python via .NET API, developers can convert all polygons to triangles in any supported 3D file.
---
{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, developers can convert all polygons to triangles in any supported 3D file.

{{% /alert %}}
##  **Olyonvert ll ll olyأوليغونز إلى riri**
لقد أضفنا زيادة كبيرة أخرى على طريقة `triangulate` في فئة [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) والتي تأخذ كائن فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) كمعلمة كما هو موضح في مثال الرمز هذا:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import PolygonModifier

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load an existing 3D file
scene = Scene("data-dir"  + "document.fbx")
#  Triangulate a scene
PolygonModifier.triangulate(scene)
#  Save 3D scene
scene.save("out"  + "triangulated_out.fbx", FileFormat.FBX7400ASCII)

{{< /highlight >}}
