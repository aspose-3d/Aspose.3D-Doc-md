---
title: Konvertera ett enda objekt i 3D fil i PLY
type: docs
weight: 20
url: /sv/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: De överbelastade EncodeMesh-medlemmarna som exponeras av PlyFormat-klassen kan användas för att konvertera mesh för ett 3D-objekt till PLY fil. EncodeMesh medlemmar tar Mesh, utdatafilnamn och PlySaveOptions objekt som parametrar. Med PLY sparningsalternativ kan utvecklare ändra namnet på koordinatkomponenter.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API tillåter utvecklare att konvertera mesh för ett enda 3D objekt i filen PLY.

{{% /alert %}}
##  **Skapa ett 3D-objekt och spara det i PLY-filen**
De överbelastade `encodeMesh` medlemmar som exponerats av klassen `PlyFormat` kan användas för att konvertera mesh i ett 3D objekt till PLY filen .. `encodeMesh` medlemmarna tar `Mesh`, utfilnamnet och `PlySaveOptions` objekt som parametrar. Med PLY sparningsalternativ kan utvecklare ändra namnet på koordinatkomponenter.
###  **Programmeringsprova**
Det här kodexemplet skapar ett 3D Cylinderobjekt och kodar sedan i filen PLY.

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
