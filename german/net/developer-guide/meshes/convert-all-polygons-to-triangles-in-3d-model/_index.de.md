---
title: Alle Polygone in Dreiecke in 3D Modell konvertieren
type: docs
weight: 50
url: /de/net/convert-all-polygons-to-triangles-in-3d-model/
description: Mit Aspose.3D for .NET API können Entwickler alle Polygone in Dreiecke in jeder unterstützten 3D-Datei konvertieren.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](http://products.aspose.com/3d/net) API können Entwickler alle Polygone in Dreiecke in jeder unterstützten 3D-Datei konvertieren.

{{% /alert %}}
##  **Alle Polygone zu Dreiecke konvertieren**
Wir haben eine weitere Überlastung der `Triangulate`-Methode in der [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-Klasse hinzugefügt, die ein [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klassen objekt als Parameter verwendet, wie in diesem Code beispiel gezeigt:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = Scene.FromFile("document.fbx");
// Triangulate a scene
PolygonModifier.Triangulate(scene);
// Save 3D scene
scene.Save("triangulated_out.fbx");

{{< /highlight >}}
