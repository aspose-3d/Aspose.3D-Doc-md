---
title: Преобразовать все многоугольники в треугольники в модели 3D
type: docs
weight: 10
url: /ru/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: Используя Aspose.3D for Python via .NET API, разработчики могут конвертировать все многоугольники в треугольники в любом поддерживаемым файле 3D.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, разработчики могут конвертировать все многоугольники в треугольники в любом поддерживаемым файле 3D.

{{% /alert %}}
##  **Конвертировать Все полигоны в треугольники**
Мы добавили еще одну перегрузку метода `triangulate` в класс [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), который принимает объект класса [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) в качестве параметра, как показано в этом примере кода:

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
