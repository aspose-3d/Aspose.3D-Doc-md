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

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
##  **Flip Coordinate System in 3D formati**
Aspose.3D for Python via .NET API consente agli utenti di capovolgere il sistema di coordinate nei formati OBJ, 3DS, STL e U3D.

{{% alert color="primary" %}} 

Per importare un file 3ds e salvarlo in formato OBJ, la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) viene utilizzata nel codice.

{{% /alert %}} 

In questo esempio, abbiamo capovolto il sistema di coordinate durante l'importazione del file 3ds e lo abbiamo salvato in formato OBJ senza materiali.
