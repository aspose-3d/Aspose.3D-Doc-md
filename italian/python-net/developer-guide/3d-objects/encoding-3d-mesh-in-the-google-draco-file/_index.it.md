---
title: Codifica 3D mesh nel file Google Draco
type: docs
weight: 60
url: /it/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API consente agli sviluppatori di importare un modello 3D e quindi codificare le mesh nei file Google Draco. Gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API consente agli sviluppatori di [Importare un modello 3D](/3d/it/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene) e quindi codificare le mesh nei file Google Draco. Gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.

{{% /alert %}}
##  **Recupera una mesh 3D e codifica in file Google Draco**
Il metodo `encode` esposto dalla classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) può essere utilizzato per codificare una mesh 3d nel file Google Draco. Ci vogliono oggetti [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) e [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) come parametri. Utilizzando le opzioni di salvataggio Draco, gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.
###  **Campione di programmazione**
Questo esempio di codice recupera una mesh di sfera e quindi codifica nel file Google Draco dopo aver specificato un livello di compressione.

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
