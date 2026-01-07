---
title: Crear escena con formas 3D primitivas
type: docs
weight: 20
url: "/es/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: Aspose.3D para Node.js a través de la API de Java tiene soporte de formas 3D primitivas. Todos los primitivos parametrizados se convertirán a malla automáticamente al guardar en cualquier formato de archivo de salida compatible.
---

{{% alert color="primary" %}} 

Aspose.3D para Node.js vía API Java tiene soporte de formas 3D primitivas. Todas las primitivas parametrizadas se convertirán a malla automáticamente al guardar en cualquier formato de archivo de salida compatible.

{{% /alert %}} 
## **Construir Escena desde Formas 3D Primitivas**
El modelado es el proceso de pura creación y la API Aspose.3D admite la creación de una escena con formas 3D primitivas.
### **Ejemplo de Programación**
Este ejemplo de código crea una escena con formas 3D primitivas y la guarda en el archivo OBJ.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar una escena 3D
var scene = new aspose.threed.Scene();

// Crear un modelo Box
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Crear un modelo Cylinder
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Guardar dibujo en el formato OBJ
scene.save("test.obj");


{{< /highlight >}}