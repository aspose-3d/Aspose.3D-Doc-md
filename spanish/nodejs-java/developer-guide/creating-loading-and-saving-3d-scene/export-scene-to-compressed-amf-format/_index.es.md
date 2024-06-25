---
title: Exportar escena a formato AMF comprimido
type: docs
weight: 60
url: /es/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java ofrece la clase AmfSaveOptions que le permite establecer el valor booleano para la compresión según sus requisitos.
---
#  **Exportar escena a formato AMF comprimido**
Aspose.3D for Node.js via Java ofrece la clase `AmfSaveOptions` que le permite establecer el valor booleano para la compresión según sus requisitos. Por defecto, el valor es true. El siguiente fragmento de código muestra la funcionalidad completa para generar un archivo de formato AMF comprimido:

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();

var node=scene.getRootNode().createChildNode(box);

node.getTransform().setScale(new aspose.threed.Vector3(12, 17, 12));
node.getTransform().setTranslation(new aspose.threed.Vector3(10, 1, 0));

var opt =new aspose.threed.AmfSaveOptions();
opt.setEnableCompression(false);

scene.save("test.amf");

{{< /highlight >}}
