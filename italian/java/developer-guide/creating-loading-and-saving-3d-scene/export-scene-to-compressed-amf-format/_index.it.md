---
title: Esporta la scena nel formato AMF compresso
type: docs
weight: 60
url: /it/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java offre la classe AmfSaveOptions che ti consente di impostare il valore booleano per la compressione secondo le tue esigenze.
---
#  **Esporta la scena nel formato AMF compresso**
Aspose.3D for Java offre una classe `AmfSaveOptions` che ti consente di impostare il valore booleano per la compressione secondo le tue esigenze. Per impostazione predefinita il valore è impostato su true. Il seguente frammento di codice mostra la funzionalità completa per generare file in formato AMF compresso:

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
