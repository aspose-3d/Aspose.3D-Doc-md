---
title: Экспорт сцены в сжатый формат AMF
type: docs
weight: 60
url: /ru/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java предлагает класс AmfSaveOptions, который позволяет вам установить логическое значение для сжатия в соответствии с вашими требованиями.
---
#  **Экспорт сцены в сжатый формат AMF**
Aspose.3D for Java предлагает класс `AmfSaveOptions`, который позволяет вам установить логическое значение для сжатия в соответствии с вашими требованиями. По умолчанию значение имеет значение true. Следующий фрагмент кода показывает полную функциональность для создания сжатого файла формата AMF:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
Scene scene = new Scene();
Box box = new Box();
Transform tr = scene.getRootNode().createChildNode(box).getTransform();
tr.setScale(new Vector3(12, 12, 12));
tr.setTranslation(new Vector3(10, 0, 0));
tr = scene.getRootNode().createChildNode(box).getTransform();
tr.setScale(new Vector3(5, 5, 5));
tr.setEulerAngles(new Vector3(50, 10, 0));
scene.getRootNode().createChildNode();
scene.getRootNode().createChildNode().createChildNode(box);
scene.getRootNode().createChildNode().createChildNode(box);
AMFSaveOptions opt = new AMFSaveOptions();
opt.setEnableCompression(false);
scene.save(MyDir + "test.amf", opt);

{{< /highlight >}}
