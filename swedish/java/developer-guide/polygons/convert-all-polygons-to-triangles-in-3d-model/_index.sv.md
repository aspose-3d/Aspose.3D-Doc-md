---
title: Konvertera alla polygoner till trianglar i 3D Modell
type: docs
weight: 10
url: /sv/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API has support of converting all polygons to triangles in any supported 3D document.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API has support of converting all polygons to triangles in any supported 3D document.

{{% /alert %}} 
##  **Konvertera alla polygoner till triangler**
Vi har lagt till en annan överbelastning av triangulerat metod i klassen `PolygonModifier` som tar ett `Scene` klassobjekt som en parameter som visas i den här co. Exempel:

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
