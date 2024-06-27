---
title: Esporta la scena nel formato AMF compresso
type: docs
weight: 60
url: /it/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java offre la classe AmfSaveOptions che ti consente di impostare il valore booleano per la compressione secondo le tue esigenze.
---
#  **Esporta la scena nel formato AMF compresso**
Aspose.3D for Node.js via Java offre una classe `AmfSaveOptions` che ti consente di impostare il valore booleano per la compressione secondo le tue esigenze. Per impostazione predefinita il valore è impostato su true. Il seguente frammento di codice mostra la funzionalità completa per generare file in formato AMF compresso:

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
