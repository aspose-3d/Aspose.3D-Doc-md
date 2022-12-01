---
title: Convertire Mesh di un singolo oggetto 3D nel file PLY
type: docs
weight: 20
url: /it/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: I membri EncodeMesh sovraccaricati esposti dalla classe PlyFormat possono essere utilizzati per convertire la mesh di un oggetto 3D in file PLY. I membri EncodeMesh prendono il nome mesh, il nome del file di output e gli oggetti PlySaveOptions come parametri. Utilizzando le opzioni di salvataggio PLY, gli sviluppatori possono cambiare il nome dei componenti coordinati.
---
{{% alert color="primary" %}}

[Aspose.3D per Python via .NET](https://products.aspose.com/3d/python-net/)API consente agli sviluppatori di convertire la mesh di un singolo oggetto 3D nel file PLY.

{{% /alert %}}
## **Creare un oggetto 3D e salvarlo in file PLY**
I membri `encodeMesh` sovraccarichi esposti dalla classe `PlyFormat` possono essere utilizzati per convertire la mesh di un oggetto 3D in file PLY. I membri `encodeMesh` prendono lo `Mesh`, il nome del file di output e gli oggetti `PlySaveOptions` come parametri. Utilizzando le opzioni di salvataggio PLY, gli sviluppatori possono cambiare il nome dei componenti coordinati.
### **Campione di programmazione**
Questo esempio di codice crea un oggetto Cilindro 3D e quindi codifica nel file PLY.

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
