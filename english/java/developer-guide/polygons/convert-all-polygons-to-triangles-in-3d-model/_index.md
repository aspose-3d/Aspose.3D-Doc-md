---
title: Convert all Polygons to Triangles in 3D Model
type: docs
weight: 10
url: /java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API has support of converting all polygons to triangles in any supported 3D document.
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support of converting all polygons to triangles in any supported 3D document.

{{% /alert %}} 
## **Convert all Polygons to Triangles**
We have added another overload of triangulate method in the `PolygonModifier` class which takes a `Scene` class object as a parameter as shown in this code example:

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
