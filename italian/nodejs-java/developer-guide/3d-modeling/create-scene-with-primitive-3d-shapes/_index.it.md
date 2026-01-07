---
title: Crea scena con forme 3D primitive
type: docs
weight: 20
url: "/it/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: Aspose.3D per Node.js tramite API Java supporta le forme 3D primitive. Tutti i primitivi parametrizzati verranno convertiti in mesh automaticamente durante il salvataggio in qualsiasi formato di file di output supportato.
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API ha il supporto di forme 3D primitive. Tutte le primitive parametrizzate saranno convertite in mesh automaticamente durante il salvataggio in qualsiasi formato di file di output supportato.

{{% /alert %}} 
## **Costruisci Scena da Forme 3D Primitive**
La modellazione è il processo di pura creazione e l'API Aspose.3D supporta la creazione di una scena con forme 3D primitive.
### **Esempio di Programmazione**
Questo esempio di codice crea una scena con forme 3D primitive e la salva nel file OBJ.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza una scena 3D
var scene = new aspose.threed.Scene();

// Crea un modello Box
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Crea un modello Cylinder
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Salva il disegno nel formato OBJ
scene.save("test.obj");


{{< /highlight >}}