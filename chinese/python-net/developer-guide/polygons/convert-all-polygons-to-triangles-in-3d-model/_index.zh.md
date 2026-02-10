---
title: 将 3D 模型中的所有多边形转换为三角形
type: docs
weight: 10
url: /zh/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: 使用 Aspose.3D for Python via .NET API，开发人员可以在任何受支持的 3D 文件中将所有多边形转换为三角形。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API，开发人员可以在任何受支持的 3D 文件中将所有多边形转换为三角形。

{{% /alert %}}
##  **将所有多边形转换为三角形**
我们在 [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) 类中添加了另一个 `triangulate` 方法的重载，它将 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类对象作为参数，如下面的代码示例所示:

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
