---
title: Aggiungi informazioni sull'asset al documento 3D
type: docs
weight: 10
url: /it/java/add-asset-information-to-3d-document/
description: I metadati sono informazioni strutturate che descrivono, spiegano, individuano o semplificano il recupero, l'utilizzo o la gestione di una risorsa di informazioni. Aspose.3D for Java API supporta la definizione dei Metadati per la scena.
---
##  **Aggiungi informazioni sull'asset al documento 3D**
I metadati sono informazioni strutturate che descrivono, spiegano, individuano o semplificano il recupero, l'utilizzo o la gestione di una risorsa di informazioni. Aspose.3D for Java API supporta la definizione dei Metadati per la scena.
###  **Definire un metadato per la scena**
3D mostra la produzione di enormi quantità di metadati e informazioni sull'immagine. I metadati sono una risorsa e fanno parte dello spettacolo.

1. Inizializza una scena 3D utilizzando la classe `Scene`.
1. Imposta il nome dell'applicazione/strumento.
1. Imposta il nome del fornitore dell'applicazione/strumento.
1. Impostare l'unità di misura.
1. Impostare il fattore di scala dell'unità di misura.
1. Salva 3D scena nel formato file supportato.

In questo esempio, supponiamo che la scena sia creata da uno strumento CAD chiamato "Egitto" ed è progettata da Manualdesk:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
