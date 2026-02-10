---
title: Konvertera alla polygoner till trianglar i 3D Modell
type: docs
weight: 50
url: /sv/net/convert-all-polygons-to-triangles-in-3d-model/
description: Använder Aspose. 3D for .NET API, utvecklare kan konvertera alla polygoner till trianglar i vilken 3D fil som stöds.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](http://products.aspose.com/3d/net) API kan utvecklare konvertera alla polygoner till trianglar i vilken 3D-fil som stöds.

{{% /alert %}}
##  **Konvertera alla polygoner till triangler**
Vi har lagt till en annan överbelastning av `Triangulate`-metoden i [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-klassen som tar ett [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-objekt som en parameter som visas i Detta kodexempel

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
