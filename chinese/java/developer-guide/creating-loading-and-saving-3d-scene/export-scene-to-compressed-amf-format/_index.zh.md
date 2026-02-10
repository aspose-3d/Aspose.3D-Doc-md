---
title: 将场景导出为压缩的 AMF 格式
type: docs
weight: 60
url: /zh/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java 提供AmfSaveOptions类，允许您根据需要设置压缩的布尔值。
---
#  **将场景导出为压缩的 AMF 格式**
Aspose。3D for Java 提供 `AmfSaveOptions` 类，允许您根据需要设置压缩的布尔值。默认情况下，该值设置为true。以下代码段显示了生成压缩的 AMF 格式文件的完整功能:

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
