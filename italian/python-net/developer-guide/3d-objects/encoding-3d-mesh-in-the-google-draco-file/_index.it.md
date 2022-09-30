---
title: Codifica 3D Mesh nel file Google Draco
type: docs
weight: 60
url: /it/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D per Python via .NET API consente agli sviluppatori di importare un modello 3D e quindi codificare le mesh nei file Google Draco. Gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.
---
{{% alert color="primary" %}}

[Aspose.3D per Python via .NET](https://products.aspose.com/3d/python-net/)API permette agli sviluppatori di[Importare un modello 3D](/3d/it/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), E quindi codificare le mesh nei file Google Draco. Gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.

{{% /alert %}}
## **Recuperare una mesh 3D e codificare in un file Google Draco**
Il metodo `encode` esposto dalla classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) può essere utilizzato per codificare una mesh 3d nel file Google Draco. Ci vogliono gli oggetti [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) e [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) come parametri. Utilizzando le opzioni di salvataggio Draco, gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.
### **Campione di programmazione**
Questo esempio di codice recupera una mesh of Sphere e quindi codifica nel file Google Draco dopo aver specificato un livello di compressione.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
