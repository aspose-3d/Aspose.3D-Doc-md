---
title: Codierung von 3D Mesh in der Google Draco-Datei
type: docs
weight: 60
url: /de/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API ermöglicht es Entwicklern, ein 3D-Modell zu importieren und dann Maschen in den Google Draco-Dateien zu codieren. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API ermöglicht es Entwicklern, [Ein 3D-Modell importieren](/3d/de/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene) zu codieren und dann Netze in den Google Draco-Dateien zu codieren. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.

{{% /alert %}}
##  **Ein 3D-Netz abrufen und in Google Draco-Datei codieren**
Die `Encode`-Methode, die von der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse angezeigt wird, kann verwendet werden, um ein 3D-Netz in der Google Draco-Datei zu codieren. Als Parameter werden Objekte im Wert von [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) und [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) benötigt. Mithilfe der Speicher optionen für Draco können Entwickler auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor ein Netz codiert wird.
###  **Programmier probe**
Dieses Code beispiel ruft eine `Mesh` von `Sphere` ab und codiert dann in der Google Draco Datei, nachdem Sie eine Kom primi erungs stufe angegeben haben.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
            
// Create a sphere
var sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
var b = FileFormat.Draco.Encode(sphere.ToMesh(), 
    new DracoSaveOptions() { CompressionLevel = DracoCompressionLevel.Optimal });
// Save the raw bytes to file
File.WriteAllBytes(RunExamples.GetOutputFilePath("SphereMeshtoDRC_Out.drc"), b);

{{< /highlight >}}
