---
title: Konvertieren Sie Mesh eines einzelnen 3D-Objekts in PLY-Datei
type: docs
weight: 20
url: /de/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Die überladenen EncodeMesh-Mitglieder, die von der Ply Format-Klasse freigelegt werden, können verwendet werden, um das Mesh eines 3D-Objekts in eine PLY-Datei zu konvertieren. Die EncodeMesh-Mitglieder verwenden die Objekte Mesh, Ausgabe dateiname und PlySaveOptions als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API ermöglicht es Entwicklern, das Mesh eines einzelnen 3D-Objekts in der PLY-Datei zu konvertieren.

{{% /alert %}}
##  **Erstellen Sie ein 3D-Objekt und speichern Sie es in einer PLY-Datei**
Die überladenen `EncodeMesh`-Mitglieder, die von der `PlyFormat`-Klasse ausgesetzt sind, können verwendet werden, um die `Mesh` eines 3D-Objekts in PLY-Datei zu konvertieren. Die `EncodeMesh`-Mitglieder nehmen die `Mesh`-, Ausgabe dateiname und `PlySaveOptions`-Objekte als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
###  **Programmier probe**
In diesem Code beispiel wird ein 3D-Cylinder-Objekt erstellt und dann in der PLY-Datei codiert.

**C#**

{{< highlight "java" >}}

 // Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

/* using Ply save options*/

//Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
