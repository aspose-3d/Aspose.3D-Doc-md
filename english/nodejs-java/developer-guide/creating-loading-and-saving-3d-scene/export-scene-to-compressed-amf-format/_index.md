---
title: Export Scene to Compressed AMF Format
type: docs
weight: 60
url: /nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java offers AmfSaveOptions class which allows you to set boolean value for compression as per your requirements. 
---

# **Export Scene to Compressed AMF Format**
Aspose.3D for Node.js via Java offers `AmfSaveOptions` class which allows you to set boolean value for compression as per your requirements. By default the value is set to true. Following code snippet shows complete functionality to generate compressed AMF format file:

{{< highlight java >}}

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();

var node=scene.getRootNode().createChildNode(box);

node.getTransform().setScale(new aspose.threed.Vector3(12, 17, 12));
node.getTransform().setTranslation(new aspose.threed.Vector3(10, 1, 0));

var opt =new aspose.threed.AmfSaveOptions();
opt.setEnableCompression(false);

scene.save("test.amf");

{{< /highlight >}}
