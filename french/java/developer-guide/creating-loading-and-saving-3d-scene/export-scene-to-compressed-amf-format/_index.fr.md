---
title: Exporter la scène au format compressé AMF
type: docs
weight: 60
url: /fr/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java offre la classe AmfSaveOptions qui vous permet de définir une valeur booléenne pour la compression selon vos besoins.
---
#  **Exporter la scène au format compressé AMF**
Aspose.3D for Java offre une classe `AmfSaveOptions` qui vous permet de définir une valeur booléenne pour la compression selon vos besoins. Par défaut, la valeur est définie sur true. L'extrait de code suivant montre la fonctionnalité complète pour générer un fichier au format AMF compressé:

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
