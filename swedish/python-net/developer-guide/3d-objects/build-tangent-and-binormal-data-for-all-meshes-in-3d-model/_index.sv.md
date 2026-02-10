---
title: Bygg Tangent- och Binormaldata för alla meshes i 3D Modell
type: docs
weight: 10
url: /sv/python-net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Genom att använda Aspose.3D for Python via .NET API kan utvecklare bygga tangent och binormal data för alla maskor i vilken 3D-fil som stöds.
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API kan utvecklare bygga tangent och binormal data för alla maskor i vilken 3D-fil som stöds.

{{% /alert %}}
##  **Bygg Tangent och Binormal data för mesh**
Vi har lagt till två BuildTangentBinormal metoder i klassen [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier). En metod tar [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klassobjektet som en parameter och en annan tar [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) klassobjektet som en parameter som visas i den här co. Exempel:

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
