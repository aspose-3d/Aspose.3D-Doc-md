---
title: مشهد التصدير إلى تنسيق مضغوط AMF
type: docs
weight: 60
url: /ar/nodejs-java/export-scene-to-compressed-amf-format/
description: يقدم Aspose.3D for Node.js via Java فئة AmfSaveOptions التي تسمح لك بتعيين القيمة المنطقية للضغط وفقًا لمتطلباتك.
---
#  **مشهد التصدير إلى تنسيق مضغوط AMF**
يقدم Aspose.3D for Node.js via Java فئة `AmfSaveOptions` التي تسمح لك بتعيين القيمة المنطقية للضغط وفقًا لمتطلباتك. افتراضيًا ، يتم تعيين القيمة إلى true. يعرض مقتطف الشفرة التالي وظائف كاملة لإنشاء ملف تنسيق AMF مضغوط:

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
