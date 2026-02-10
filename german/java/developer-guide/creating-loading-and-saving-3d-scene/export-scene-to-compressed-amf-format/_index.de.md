---
title: Szene in komprimiertes AMF-Format exportieren
type: docs
weight: 60
url: /de/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java bietet die AmfSaveOptions-Klasse, mit der Sie den booleschen Wert für die Kom primi erung gemäß Ihren Anforderungen festlegen können.
---
#  **Szene in komprimiertes AMF-Format exportieren**
Aspose.3D for Java bietet die `AmfSaveOptions`-Klasse, mit der Sie den booleschen Wert für die Kom primi erung gemäß Ihren Anforderungen festlegen können. Standard mäßig ist der Wert auf true gesetzt. Das folgende Code-Snippet zeigt die vollständige Funktional ität zum Generieren einer komprimierten AMF-Format datei:

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
