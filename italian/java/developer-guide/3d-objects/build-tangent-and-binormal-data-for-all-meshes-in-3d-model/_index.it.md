---
title: Costruisci dati tangente e binormale per tutte le maglie nel modello 3D
type: docs
weight: 10
url: /it/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Con Aspose.3D for Java API, gli sviluppatori possono creare dati tangenti e binormali per tutte le mesh in qualsiasi documento 3D supportato.
---
{{% alert color="primary" %}} 

Con Aspose.3D for Java API, gli sviluppatori possono creare dati tangenti e binormali per tutte le mesh in qualsiasi documento 3D supportato.

{{% /alert %}} 
##  **Costruisci dati Tangenti e Binormal per Mesh**
Abbiamo aggiunto due metodi `buildTangentBinormal` nella classe `PolygonModifier`. Un metodo prende l'oggetto della classe `Scene` come parametro e un altro prende l'oggetto della classe `Mesh` come parametro, come mostrato in questo esempio di codice:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene( MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.buildTangentBinormal(scene);
// Save 3D scene
scene.save(MyDir + "BuildTangentAndBinormalData_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
