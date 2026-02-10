---
title: Exportar escena a formato AMF comprimido
type: docs
weight: 60
url: /es/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java ofrece la clase AmfSaveOptions que le permite establecer el valor booleano para la compresión según sus requisitos.
---
#  **Exportar escena a formato AMF comprimido**
Aspose.3D for Java ofrece la clase `AmfSaveOptions` que le permite establecer el valor booleano para la compresión según sus requisitos. Por defecto, el valor es true. El siguiente fragmento de código muestra la funcionalidad completa para generar un archivo de formato AMF comprimido:

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
