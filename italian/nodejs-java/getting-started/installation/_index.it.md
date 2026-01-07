---
title: Installation
type: docs
weight: 40
url: /it/nodejs-java/installation/
---
##  **Requisiti di sistema**

Innanzitutto, devi controllare e confermare che le specifiche della macchina soddisfano [Requisiti di sistema](/3d/it/nodejs-java/system-requirements/).

##  **Installazione di Aspose.3D for Node.js via Java**
`npm` è il modo più semplice per scaricare e installare [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

Per installare Aspose.3D, esegui questo comando: npm install aspose.3d

##  **Utilizzo di Aspose.3D for Node.js via Java**

Una volta completata l'installazione del modulo, puoi utilizzare Aspose.3D dal tuo codice Node.js in questo modo:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.3d");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

