---
title: Aggiungi Materiale alle Entità 3D
type: docs
weight: 60
url: "/it/nodejs-java/add-material-to-3d-entities/"
description: "PBR svolge un ruolo fondamentale per la grafica del motore di gioco, con il suo rendering efficiente e realistico delle interazioni tra luce e superficie tramite l'attenuazione della luminosità e la dispersione della luce riflessa. Gli sviluppatori possono utilizzare l'API Aspose.3D per applicare un materiale PBR a oggetti 3D in una scena. Questo esempio di codice dimostra come creare un oggetto Box e quindi applicare il materiale PBR."
---

{{% alert color="primary" %}}

PBR svolge un ruolo chiave per la grafica del motore di gioco, con la sua efficiente e realistica resa delle interazioni tra luce e superficie tramite l'attenuazione della luminosità e la dispersione della luce riflessa. Gli sviluppatori possono utilizzare l'API Aspose.3D per applicare un materiale PBR a oggetti 3D in una scena. Questo esempio di codice dimostra come creare un oggetto Box e quindi applicare il materiale PBR.

{{% /alert %}}


## **Applica un Materiale di Rendering Fisicamente Corretto (PBR) a un Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// inizializza una scena
var scene = new aspose.threed.Scene();

// inizializza l'oggetto materiale PBR
var mat = new aspose.threed.PbrMaterial();

// un materiale quasi metallico
mat.setMetallicFactor(0.9);

// la superficie del materiale è molto ruvida
mat.setRoughnessFactor(0.9);

// crea un box a cui verrà applicato il materiale
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// salva la scena 3D in formato USDZ
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}