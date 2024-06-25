---
title: Konvertieren Sie Mesh eines einzelnen 3D-Objekts in PLY-Datei
type: docs
weight: 20
url: /de/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Die überladenen EncodeMesh-Mitglieder, die von der Ply Format-Klasse freigelegt werden, können verwendet werden, um das Mesh eines 3D-Objekts in eine PLY-Datei zu konvertieren. Die EncodeMesh-Mitglieder verwenden die Objekte Mesh, Ausgabe dateiname und PlySaveOptions als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API ermöglicht es Entwicklern, das Mesh eines einzelnen 3D-Objekts in der PLY-Datei zu konvertieren.

{{% /alert %}}
##  **Erstellen Sie ein 3D-Objekt und speichern Sie es in einer PLY-Datei**
Die überladenen `encodeMesh`-Mitglieder, die von der `PlyFormat`-Klasse angezeigt werden, können verwendet werden, um das Mesh eines 3D-Objekts in eine PLY-Datei zu konvertieren. Die `encodeMesh`-Mitglieder nehmen die `Mesh`-, Ausgabe dateiname und `PlySaveOptions`-Objekte als Parameter. Mit den Speicher optionen PLY können Entwickler den Namen der Koordinaten komponenten ändern.
###  **Programmier probe**
In diesem Code beispiel wird ein 3D-Cylinder-Objekt erstellt und dann in der PLY-Datei codiert.

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
