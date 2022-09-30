---
title: Codificación 3D Malla en el archivo Google Draco
type: docs
weight: 30
url: /es/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API tiene soporte para importar el modelo 3D, recuperar malla y luego codificar malla en el archivo Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para importar el modelo 3D, recuperar malla y luego codificar malla en el archivo Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.

{{% /alert %}} 
## **Recuperar la malla 3D y codificar en el archivo Google Draco**
El método de codificación expuesto por la clase `DracoFormat` se puede utilizar para codificar una malla 3D en el archivo Google Draco. Toma como parámetros los objetos `Mesh` y `DracoSaveOptions`. Con las opciones de guardado Draco, los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
### **Muestra de programación**
Este ejemplo de código recupera Mesh of Sphere y, a continuación, codifique en el archivo Google Draco después de especificar un nivel de compresión.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-Encode3DMeshinGoogleDraco.java" >}}
