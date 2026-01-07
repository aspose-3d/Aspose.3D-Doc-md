---
title: Añadir información de activos al documento 3D
type: docs
weight: 10
url: "/es/nodejs-java/add-asset-information-to-3d-document/"
description: Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D para Node.js a través de la API Java tiene soporte para definir metadatos para la escena.
---

## **Agregar Información de Activos a Documento 3D**
Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D para Node.js vía API de Java tiene soporte para definir Metadatos para la escena.
### **Definir un Metadato para la escena**
Los espectáculos 3D producen grandes cantidades de metadatos e información de imágenes. Los metadatos son un activo y parte del espectáculo.

1. Inicializar una escena 3D usando la clase `Scene`.
1. Establecer nombre de aplicación/herramienta.
1. Establecer nombre de proveedor de aplicación/herramienta.
1. Establecer unidad de medida.
1. Establecer factor de escala de la unidad de medida.
1. Guardar la escena 3D en un formato de archivo compatible.

En este ejemplo, asumimos que la escena es creada por una herramienta CAD llamada “Egypt” y es diseñada por “Manualdesk”:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar una escena 3D
var scene = new aspose.threed.Scene();

// Inicializar el objeto Box
var box=new aspose.threed.Box();

// Agregar el objeto Box a la escena
scene.getRootNode().createChildNode(box);

// Establecer nombre de aplicación/herramienta
scene.getAssetInfo().setApplicationName("Egypt");

// Establecer nombre de proveedor de aplicación/herramienta
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// Usamos la unidad de medida egipcia antigua Pole
scene.getAssetInfo().setUnitName("pole");

// Un Pole equivale a 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}