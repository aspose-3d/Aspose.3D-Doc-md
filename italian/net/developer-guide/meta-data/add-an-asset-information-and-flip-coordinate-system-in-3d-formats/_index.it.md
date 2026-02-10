---
title: Aggiungi informazioni sull'asset alla scena
type: docs
weight: 10
url: /it/net/add-an-asset-information-to-scene
description: I metadati sono informazioni strutturate che descrivono, spiegano, individuano o semplificano il recupero, l'utilizzo o la gestione di una risorsa di informazioni. Aspose.3D for .NET API consente agli sviluppatori di definire un Metadata per la scena.
---
##  **Aggiungi informazioni sull'asset alla scena 3D**
I metadati sono informazioni strutturate che descrivono, spiegano, individuano o semplificano il recupero, l'utilizzo o la gestione di una risorsa di informazioni. Aspose.3D for .NET API consente agli sviluppatori di definire un Metadata per la scena.
###  **Definire un metadato per la scena**
3D mostra la produzione di enormi quantità di metadati e informazioni sull'immagine. I metadati sono una risorsa e fanno parte dello spettacolo.

1. Inizializza una scena 3D utilizzando la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene).
1. Imposta il nome dell'applicazione/strumento.
1. Imposta il nome del fornitore dell'applicazione/strumento.
1. Impostare l'unità di misura.
1. Impostare il fattore di scala dell'unità di misura.
1. Salva 3D scena nel formato file supportato.

In questo esempio, supponiamo che la scena sia creata da uno strumento CAD chiamato "Egitto" ed è progettata da Manualdesk:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a 3D scene
Scene scene = new Scene();

// Set application/tool name
scene.AssetInfo.ApplicationName = "Egypt";

// Set application/tool vendor name
scene.AssetInfo.ApplicationVendor = "Manualdesk";

// We use ancient egyption measurement unit Pole
scene.AssetInfo.UnitName = "pole";

// One Pole equals to 60cm
scene.AssetInfo.UnitScaleFactor = 0.6;

// Save scene to 3D supported file formats
scene.Save("InformationToScene.fbx");

{{< /highlight >}}
