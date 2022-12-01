---
title: Codierung 3D Mesh in der Google Draco Datei
type: docs
weight: 60
url: /de/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API ermöglicht es Entwicklern, ein 3D-Modell zu importieren und dann Maschen in den Google Draco-Dateien zu codieren. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API ermöglicht es Entwicklern[Importieren Sie ein Modell 3D](/3d/de/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene)Und codieren Sie dann Maschen in den Dateien Google Draco. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.

{{% /alert %}}
## **Holen Sie ein 3D Mesh und Codieren in Google Draco Datei**
Die `Encode`-Methode, die von der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse verfügbar ist, kann verwendet werden, um ein 3D-Netz in der Datei Google Draco zu codieren. Als Parameter werden Objekte [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) und [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) benötigt. Mithilfe der Speicher optionen Draco können Entwickler auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor ein Netz codiert wird.
### **Programmier probe**
In diesem Code beispiel wird eine `Mesh` von `Sphere` abgerufen und dann in der Datei Google Draco codiert, nachdem eine Kom primi erungs stufe angegeben wurde.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.cs" >}}
