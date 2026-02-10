---
title: Tüm poligonları 3D modelinde üçgenlere dönüştürün
type: docs
weight: 10
url: /tr/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: Using Aspose.3D for Python via .NET API, developers can convert all polygons to triangles in any supported 3D file.
---
{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, developers can convert all polygons to triangles in any supported 3D file.

{{% /alert %}}
##  **Tonvert All olyolygons Triangles**
Bu kod örneğinde gösterildiği gibi bir parametre olarak [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıf nesnesini alan [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) sınıfında `triangulate` yönteminin başka bir aşırı yüklenmesini ekledik:

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
