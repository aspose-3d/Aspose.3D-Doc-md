---
title: Alle Polygone in Dreiecke in 3D Modell konvertieren
type: docs
weight: 10
url: /de/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API unterstützt die Konvertierung aller Polygone in Dreiecke in jedem unterstützten 3D-Dokument.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API unterstützt die Konvertierung aller Polygone in Dreiecke in jedem unterstützten 3D-Dokument.

{{% /alert %}} 
##  **Alle Polygone zu Dreiecke konvertieren**
Wir haben eine weitere Überlastung der Triangulate in der `PolygonModifier`-Klasse hinzugefügt, die ein `Scene`-Klassen objekt als Parameter verwendet, wie in diesem Code beispiel gezeigt:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene(MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.triangulate(scene);
// Save 3D scene
scene.save(MyDir + "triangulated_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
