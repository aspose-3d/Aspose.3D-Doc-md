---
title: Szene in komprimiertes AMF-Format exportieren
type: docs
weight: 60
url: /de/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java bietet die AmfSaveOptions-Klasse, mit der Sie den booleschen Wert für die Kom primi erung gemäß Ihren Anforderungen festlegen können.
---
#  **Szene in komprimiertes AMF-Format exportieren**
Aspose.3D for Node.js via Java bietet eine `AmfSaveOptions`-Klasse, mit der Sie den booleschen Wert für die Kom primi erung gemäß Ihren Anforderungen festlegen können. Standard mäßig ist der Wert auf true gesetzt. Das folgende Code-Snippet zeigt die vollständige Funktional ität zum Generieren einer komprimierten AMF-Format datei:

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
