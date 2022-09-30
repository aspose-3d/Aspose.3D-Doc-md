---
title: Konvertera Mesh för ett enda 3D objekt i PLY
type: docs
weight: 20
url: /sv/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Den överbelastade EncodeMesh medlemmar som exponeras av PlyFormat klassen kan användas för att konvertera mesh av en 3D objekt. till PLY. EncodeMesh medlemmar tar Mesh, utdatafilnamn och PlySaveOptions objekt som parametrar. Med hjälp av PLY sparalternativ kan utvecklare ändra namnet på koordinatkomponenter.
---
{{% alert color="primary" %}}

[Aspose.3D för Python via .NET](https://products.aspose.com/3d/python-net/)API tillåter utvecklare att konvertera Mesh av en enda 3D objekt i filen PLY.

{{% /alert %}}
## **Skapa ett 3D objekt och spara det till PLY-fil.**
De överbelastade `encodeMesh` medlemmar som exponeras av klassen `PlyFormat` kan användas för att konvertera Mesh av en 076123488 1 objekt till PLY-fil. De `encodeMesh` medlemmar tar `Mesh`, utdata filnamn och `PlySaveOptions` objekt som parametrar. Med hjälp av PLY sparalternativ kan utvecklare ändra namnet på koordinatkomponenter.
### **Programmeringsprova**
Detta kodexempel skapar ett 3D Cylinderobjekt, och sedan koda i filen PLY.

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
