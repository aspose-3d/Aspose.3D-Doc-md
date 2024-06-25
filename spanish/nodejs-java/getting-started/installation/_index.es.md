---
title: Installation
type: docs
weight: 40
url: /es/nodejs-java/installation/
---
##  **Requisitos del sistema**

Primero, debe verificar y confirmar que las especificaciones de la máquina cumplen con [Requisitos del sistema](/3d/es/nodejs-java/system-requirements/).

##  **Instalación de Aspose.3D for Node.js via Java**
`npm` es la forma más fácil de descargar e instalar [Aspose.3D for Node.js via Java](https://www.npmjs.com/package/aspose.3d).

Para instalar Aspose.3D, ejecute este comando: npm install aspose.3d

##  **Usando Aspose.3D for Node.js via Java**

Una vez que termine de instalar el módulo, puede usar Aspose.3D desde su código Node.js de esta manera:

```py
var aspose = aspose || {};
aspose.threed = require("aspose.threed");

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();
scene.getRootNode().createChildNode(box);

scene.save("out.stl");
```

