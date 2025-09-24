---
title: Leer documento 3D
type: docs
weight: 30
url: "/es/nodejs-java/read-3d-document/"
description: Aspose.3D para Node.js a través de la API de Java tiene soporte para leer varios tipos de documentos 3D.
---

## **Lista de formatos 3D compatibles (importación)**
Aspose.3D para Node.js a través de la API de Java tiene soporte para leer varios tipos de documentos 3D. Los constructores disponibles de la clase `Scene` ayudan a hacerlo y aceptan una cadena de ruta de archivo válida. Los formatos de archivo legibles admitidos son los siguientes:

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
1. RVM (Texto, Binario)
1. ASE

Los constructores de la clase Scene detectan el formato del documento 3D internamente.
## **Importar documento 3D**
Aspose.3D para la API de Java tiene soporte para importar varios tipos de documentos 3D para fines de modificación, adición y procesamiento.
### **Lectura de una Escena 3D: Muestras de Programación**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inicializar un objeto de clase Scene
var scene = new aspose.threed.Scene();

// Cargar un documento 3D existente
scene.open( "document.obj");

{{< /highlight >}}