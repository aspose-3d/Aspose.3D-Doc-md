---
title: Leggi documento 3D
type: docs
weight: 30
url: "/it/nodejs-java/read-3d-document/"
description: Aspose.3D per Node.js tramite API Java supporta la lettura di vari tipi di documenti 3D.
---

## **Elenco dei formati 3D supportati (importazione)**
Aspose.3D for Node.js via Java API supporta la lettura di vari tipi di documenti 3D. I costruttori disponibili della classe `Scene` aiutano a farlo e accettano una stringa di percorso file valido. I formati di file leggibili supportati sono i seguenti:

1. FBX 7.5 (ASCII, Binario)
1. FBX 7.4 (ASCII, Binario)
1. FBX 7.3 (ASCII, Binario)
1. FBX 7.2 (ASCII, Binario)
1. STL (ASCII, Binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binario)
1. X (ASCII, Binario)
1. Draco
1. 3MF
1. RVM (Testo, Binario)
1. ASE

I costruttori della classe Scene rilevano internamente il formato del documento 3D.
## **Importazione di un documento 3D**
Aspose.3D for Java API supporta l'importazione di vari tipi di documenti 3D per scopi di modifica, aggiunta ed elaborazione.
### **Lettura di una scena 3D: Esempi di programmazione**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza un oggetto classe Scene
var scene = new aspose.threed.Scene();

// Carica un documento 3D esistente
scene.open( "document.obj");

{{< /highlight >}}