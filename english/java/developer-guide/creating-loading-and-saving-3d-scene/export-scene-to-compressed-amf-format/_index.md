---
title: Export Scene to Compressed AMF Format
type: docs
weight: 60
url: /java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java offers AmfSaveOptions class which allows you to set boolean value for compression as per your requirements. 
---

# **Export Scene to Compressed AMF Format**
Aspose.3D for Java offers `AmfSaveOptions` class which allows you to set boolean value for compression as per your requirements. By default the value is set to true. Following code snippet shows complete functionality to generate compressed AMF format file:

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
