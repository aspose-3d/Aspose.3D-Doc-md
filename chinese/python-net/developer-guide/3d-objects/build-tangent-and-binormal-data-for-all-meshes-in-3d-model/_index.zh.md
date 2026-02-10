---
title: 为 3D 模型中的所有网格构建切线和二项式数据
type: docs
weight: 10
url: /zh/python-net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: 使用 Aspose.3D for Python via .NET API，开发人员可以为任何受支持的 3D 文件中的所有网格构建切线和二项式数据。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API，开发人员可以为任何受支持的 3D 文件中的所有网格构建切线和二项式数据。

{{% /alert %}}
##  **为网格构建切线和双正数据**
我们在 [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) 类中添加了两个BuildTangentBinormal方法。一个方法将 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类对象作为参数，另一个方法将 [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) 类对象作为参数，如下代码示例所示:

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
