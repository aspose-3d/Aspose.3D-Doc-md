---
title: Convertire tutti i poligoni in triangoli nel modello 3D
type: docs
weight: 10
url: /it/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API supporta la conversione di tutti i poligoni in triangoli in qualsiasi documento 3D supportato.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta la conversione di tutti i poligoni in triangoli in qualsiasi documento 3D supportato.

{{% /alert %}} 
##  **Convertire tutti i poligoni a triangoli**
Abbiamo aggiunto un altro overload del metodo triangolare nella classe `PolygonModifier` che accetta un oggetto di classe `Scene` come parametro, come mostrato in questo esempio di codice:

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
