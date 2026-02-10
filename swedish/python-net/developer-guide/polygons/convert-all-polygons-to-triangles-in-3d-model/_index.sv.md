---
title: Konvertera alla polygoner till trianglar i 3D Modell
type: docs
weight: 10
url: /sv/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: Med Aspose.3D for Python via .NET API kan utvecklare konvertera alla polygoner till trianglar i vilken 3D-fil som stöds.
---
{{% alert color="primary" %}}

Med [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API kan utvecklare konvertera alla polygoner till trianglar i vilken 3D-fil som stöds.

{{% /alert %}}
##  **Konvertera alla polygoner till triangler**
Vi har lagt till en annan överbelastning av `triangulate`-metoden i [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-klassen som tar ett [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-objekt som en parameter som visas i Detta kodexempel

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
