---
title: Построение касательных и бинонормальных данных для всех ячеек в модели 3D
type: docs
weight: 10
url: /ru/python-net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Используя Aspose.3D for Python via .NET API, разработчики могут создавать касательные и бинонормальные данные для всех ячеек в любом поддерживаемым файле 3D.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, разработчики могут создавать касательные и бинонормальные данные для всех ячеек в любом поддерживаемым файле 3D.

{{% /alert %}}
##  **Построить Tangent и Binormal данные для Mesh**
Мы добавили два метода BuildTangentBinormal в класс [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier). Один метод принимает объект класса [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) в качестве параметра, а другой-объект класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) в качестве параметра, как показано в этом примере кода:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import PolygonModifier

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load an existing 3D file
scene = Scene("data-dir"  + "document.fbx")
#  Triangulate a scene
PolygonModifier.build_tangent_binormal(scene)
#  Save 3D scene
scene.save("out"  + "BuildTangentAndBinormalData_out.fbx", FileFormat.FBX7400ASCII)

{{< /highlight >}}
