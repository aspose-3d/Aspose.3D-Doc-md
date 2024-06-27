---
title: Экспорт сцены в сжатый формат AMF
type: docs
weight: 60
url: /ru/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java предлагает класс AmfSaveOptions, который позволяет вам установить логическое значение для сжатия в соответствии с вашими требованиями.
---
#  **Экспорт сцены в сжатый формат AMF**
Aspose.3D for Node.js via Java предлагает класс `AmfSaveOptions`, который позволяет вам установить логическое значение для сжатия в соответствии с вашими требованиями. По умолчанию значение имеет значение true. Следующий фрагмент кода показывает полную функциональность для создания сжатого файла формата AMF:

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
