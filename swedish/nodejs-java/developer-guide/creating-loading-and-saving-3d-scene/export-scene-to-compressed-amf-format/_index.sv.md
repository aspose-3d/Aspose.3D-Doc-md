---
title: Exportera scen till komprimerat AMF Format
type: docs
weight: 60
url: /sv/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java erbjuder AmfSaveOptions klass som låter dig ställa in booleanskt värde för komprimering enligt dina krav.
---
#  **Exportera scen till komprimerat AMF Format**
Aspose.3D for Node.js via Java erbjuder `AmfSaveOptions` klass som låter dig ställa in boolsk värde för komprimering enligt dina krav. Som standard är värdet inställt till true. Följande kodsnutt visar fullständig funktionalitet för att skapa komprimerad AMF-formatfil:

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
