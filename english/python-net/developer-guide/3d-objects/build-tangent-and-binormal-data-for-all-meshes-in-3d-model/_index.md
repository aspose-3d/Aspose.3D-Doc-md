---
title: Build Tangent and Binormal Data for all Meshes in 3D Model
type: docs
weight: 10
url: /python-net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Using Aspose.3D for Python via .NET API, developers can build tangent and binormal data for all meshes in any supported 3D file.
---

{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, developers can build tangent and binormal data for all meshes in any supported 3D file.

{{% /alert %}}
## **Build Tangent and Binormal data for Mesh**
We have added two BuildTangentBinormal methods in the [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) class. One method takes a [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class object as a parameter and another one takes a [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object as a parameter as shown in this code example:

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
