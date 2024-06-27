---
title: Codierung von 3D Mesh in der Google Draco-Datei
type: docs
weight: 60
url: /de/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API ermöglicht es Entwicklern, ein 3D-Modell zu importieren und dann Netze in den Google Draco-Dateien zu codieren. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API ermöglicht es Entwicklern, [Ein 3D-Modell importieren](/3d/de/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene) zu codieren und dann Netze in den Google Draco-Dateien zu codieren. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.

{{% /alert %}}
##  **Ein 3D-Netz abrufen und in Google Draco-Datei codieren**
Die `encode`-Methode, die von der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse angezeigt wird, kann verwendet werden, um ein 3D-Netz in der Google Draco-Datei zu codieren. Als Parameter werden Objekte im Wert von [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) und [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) benötigt. Mithilfe der Speicher optionen für Draco können Entwickler auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor ein Netz codiert wird.
###  **Programmier probe**
In diesem Code beispiel wird ein Mesh of Sphere abgerufen und nach Angabe einer Kom primi erungs stufe in der Datei Google Draco codiert.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
