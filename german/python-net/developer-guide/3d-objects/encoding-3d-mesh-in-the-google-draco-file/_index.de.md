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

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoCompressionLevel, DracoSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a sphere
sphere = Sphere()
options = DracoSaveOptions()
options.compression_level = DracoCompressionLevel.OPTIMAL
#  Encode the sphere to Google Draco raw data using optimal compression level.
b = FileFormat.DRACO.encode(sphere.to_mesh(), options)
#  Save the raw bytes to file
with open("out"  + "SphereMeshtoDRC_Out.drc", "wb") as f:
    f.write(b)

{{< /highlight >}}
