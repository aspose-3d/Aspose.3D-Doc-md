---
title: Aggiungi informazioni sulle risorse e capovolgi il sistema di coordinate in formati 3D
type: docs
weight: 10
url: /it/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: I metadati sono informazioni strutturate che descrivono, spiegano, individuano o semplificano il recupero, l'utilizzo o la gestione di una risorsa di informazioni. Aspose.3D for Python via .NET API consente agli sviluppatori di definire un Metadato per la scena.
---
##  **Aggiungi informazioni sull'asset alla scena 3D**
I metadati sono informazioni strutturate che descrivono, spiegano, individuano o semplificano il recupero, l'utilizzo o la gestione di una risorsa di informazioni. Aspose.3D for Python via .NET API consente agli sviluppatori di definire un Metadato per la scena.
###  **Definire un metadato per la scena**
3D mostra la produzione di enormi quantità di metadati e informazioni sull'immagine. I metadati sono una risorsa e fanno parte dello spettacolo.

1. Inizializza una scena 3D utilizzando la classe `Scene`.
1. Imposta il nome dell'applicazione/strumento.
1. Imposta il nome del fornitore dell'applicazione/strumento.
1. Impostare l'unità di misura.
1. Impostare il fattore di scala dell'unità di misura.
1. Salva 3D scena nel formato file supportato.

In questo esempio, supponiamo che la scena sia creata da uno strumento CAD chiamato "Egitto" ed è progettata da Manualdesk:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Flip Coordinate System in 3D formati**
Aspose.3D for Python via .NET API consente agli utenti di capovolgere il sistema di coordinate nei formati OBJ, 3DS, STL e U3D.

{{% alert color="primary" %}} 

Per importare un file 3ds e salvarlo in formato OBJ, la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) viene utilizzata nel codice.

{{% /alert %}} 

In questo esempio, abbiamo capovolto il sistema di coordinate durante l'importazione del file 3ds e lo abbiamo salvato in formato OBJ senza materiali.
