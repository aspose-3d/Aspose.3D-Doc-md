---
title: Costruisci dati tangenti e binormali per tutte le maglie nel modello 3D
type: docs
weight: 30
url: /it/net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono creare dati tangenti e binormali per tutte le mesh in qualsiasi file 3D supportato.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](http://products.aspose.com/3d/net) API, gli sviluppatori possono creare dati tangenti e binormali per tutte le mesh in qualsiasi file 3D supportato.

{{% /alert %}}
##  **Costruisci dati Tangenti e Binormal per Mesh**
Abbiamo aggiunto due metodi BuildTangentBinormal nella classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier). Un metodo prende l'oggetto della classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) come parametro e un altro prende l'oggetto della classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) come parametro, come mostrato in questo esempio di codice:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = new Scene(RunExamples.GetDataFilePath("document.fbx"));
// Triangulate a scene
PolygonModifier.BuildTangentBinormal(scene);
// Save 3D scene
scene.Save(RunExamples.GetOutputFilePath("BuildTangentAndBinormalData_out.fbx"), FileFormat.FBX7400ASCII);

{{< /highlight >}}
