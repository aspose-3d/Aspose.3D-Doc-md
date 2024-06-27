---
title: Exporter la scène au format compressé AMF
type: docs
weight: 60
url: /fr/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java offre la classe AmfSaveOptions qui vous permet de définir une valeur booléenne pour la compression selon vos besoins.
---
#  **Exporter la scène au format compressé AMF**
Aspose.3D for Node.js via Java propose une classe `AmfSaveOptions` qui vous permet de définir une valeur booléenne pour la compression selon vos besoins. Par défaut, la valeur est définie sur true. L'extrait de code suivant montre la fonctionnalité complète pour générer un fichier au format AMF compressé:

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
