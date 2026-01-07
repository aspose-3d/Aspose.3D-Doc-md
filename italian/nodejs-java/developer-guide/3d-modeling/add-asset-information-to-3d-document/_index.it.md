---
title: Aggiungi Informazioni sugli Asset al documento 3D
type: docs
weight: 10
url: "/it/nodejs-java/add-asset-information-to-3d-document/"
description: "I metadati sono informazioni strutturate che descrivono, spiegano, localizzano o facilitano il recupero, l'utilizzo o la gestione di una risorsa informativa. Aspose.3D per Node.js via Java API supporta la definizione di metadati per la scena."
---

## **Aggiungi Informazioni sull'Asset a Documento 3D**
I metadati sono informazioni strutturate che descrivono, spiegano, localizzano o facilitano il recupero, l'uso o la gestione di una risorsa informativa. Aspose.3D per Node.js via Java API supporta la definizione di Metadati per la scena.
### **Definisci un Metadato per la scena**
Gli spettacoli 3D producono enormi quantità di metadati e informazioni sulle immagini. I metadati sono un asset e parte dello spettacolo.

1. Inizializza una Scena 3D usando la classe `Scene`.
1. Imposta il nome dell'applicazione/strumento.
1. Imposta il nome del fornitore dell'applicazione/strumento.
1. Imposta l'unità di misura.
1. Imposta il fattore di scala dell'unità di misura.
1. Salva la scena 3D nel formato di file supportato.

In questo esempio, supponiamo che la scena sia creata da un tool CAD chiamato “Egypt” ed è progettata da “Manualdesk”:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza una Scena 3D
var scene = new aspose.threed.Scene();

// Inizializza l'oggetto Box
var box=new aspose.threed.Box();

// Aggiungi l'oggetto Box alla scena
scene.getRootNode().createChildNode(box);

// Imposta il nome dell'applicazione/strumento
scene.getAssetInfo().setApplicationName("Egypt");

// Imposta il nome del fornitore dell'applicazione/strumento
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// Usiamo l'antica unità di misura egiziana Pole
scene.getAssetInfo().setUnitName("pole");

// Un Pole equivale a 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}