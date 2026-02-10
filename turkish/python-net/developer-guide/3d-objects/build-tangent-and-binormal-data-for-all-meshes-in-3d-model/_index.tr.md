---
title: Build Tangent and Binormal Data for all Meshes in 3D Model
type: docs
weight: 10
url: /tr/python-net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Aspose.3D for Python via .NET API kullanarak, geliştiriciler herhangi bir desteklenen 3D dosyasında tüm ağlar için teğet ve binormal veri oluşturabilir.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API kullanarak, geliştiriciler herhangi bir desteklenen 3D dosyasında tüm ağlar için teğet ve binormal veri oluşturabilir.

{{% /alert %}}
##  **Mesh için Tangangent ve Binormal veri**
We have added two BuildTangentBinormal methods in the [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) class. One method takes the [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class object as a parameter and another one takes the [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object as a parameter as shown in this code example:

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
