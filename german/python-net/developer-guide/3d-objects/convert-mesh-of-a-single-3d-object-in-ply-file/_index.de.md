---
title: Konvertieren Sie Mesh eines einzelnen Objekts 3D in der Datei PLY
type: docs
weight: 20
url: /de/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Die überladenen EncodeMesh-Mitglieder, die von der PlyFormat-Klasse freigelegt werden, können verwendet werden, um das Mesh eines 3D-Objekts in eine PLY-Datei zu konvertieren. Die EncodeMesh-Mitglieder verwenden die Objekte Mesh, Ausgabe datei name und PlySaveOptions als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
---
{{% alert color="primary" %}}

[Aspose.3D für Python via .NET](https://products.aspose.com/3d/python-net/)Mit API können Entwickler das Mesh eines einzelnen 3D-Objekts in der Datei PLY konvertieren.

{{% /alert %}}
## **Erstellen Sie ein Objekt 3D und speichern Sie es in der Datei PLY**
Die überladenen `encodeMesh`-Mitglieder, die von der `PlyFormat`-Klasse freigelegt werden, können verwendet werden, um das Mesh eines 3D-Objekts in eine PLY-Datei zu konvertieren. Die `encodeMesh`-Mitglieder nehmen den Namen der Ausgabe datei `Mesh` und die Objekte `PlySaveOptions` als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
### **Programmier probe**
Dieses Code beispiel erstellt ein 3D Cylinder-Objekt und codiert dann in der Datei PLY.

**Python**

```py

from aspose.threed import FileFormat, FileContentType
from aspose.threed.entities import Cylinder
from aspose.threed.formats import PlySaveOptions

# Create a cylinder object and save it to ply file

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply")

# using Ply save options

# Save as binary PLY format, the default value is ASCII

opt = PlySaveOptions(FileContentType.BINARY)

# change the components to 's' and 't'

opt.texture_coordinate_components.item1 = "s
opt.texture_coordinate_components.item2 = "t"

# save the mesh

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply", opt)

```
