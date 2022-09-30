---
title: Konvertieren Sie Mesh eines einzelnen Objekts 3D in der Datei PLY
type: docs
weight: 20
url: /de/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Die überladenen EncodeMesh-Mitglieder, die von der PlyFormat-Klasse freigelegt werden, können verwendet werden, um das Mesh eines 3D-Objekts in eine PLY-Datei zu konvertieren. Die EncodeMesh-Mitglieder verwenden die Objekte Mesh, Ausgabe datei name und PlySaveOptions als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)Mit API können Entwickler das Mesh eines einzelnen 3D-Objekts in der Datei PLY konvertieren.

{{% /alert %}}
## **Erstellen Sie ein Objekt 3D und speichern Sie es in der Datei PLY**
Die überladenen `EncodeMesh`-Mitglieder, die von der `PlyFormat`-Klasse freigelegt wurden, können verwendet werden, um die `Mesh` eines 3D-Objekts in die PLY-Datei zu konvertieren. Die `EncodeMesh`-Mitglieder nehmen den Namen der Ausgabe datei `Mesh` und die Objekte `PlySaveOptions` als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
### **Programmier probe**
Dieses Code beispiel erstellt ein 3D Cylinder-Objekt und codiert dann in der Datei PLY.

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
