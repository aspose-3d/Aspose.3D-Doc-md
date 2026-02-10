---
title: Sahneyi sıkıştırılmış AMF formatına aktar
type: docs
weight: 60
url: /tr/java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Java, gereksinimlerinize göre sıkıştırma için boole değerini ayarlamanızı sağlayan amfsaveoptions sınıfı sunar.
---
#  **Sahneyi sıkıştırılmış AMF formatına aktar**
Aspose.3D for Java, gereksinimlerinize göre sıkıştırma için boole değerini ayarlamanızı sağlayan `AmfSaveOptions` sınıfı sunar. Varsayılan olarak değer doğrudur. Kod parçacığı aşağıdaki sıkıştırılmış AMF format dosyası oluşturmak için tam işlevselliği gösterir:

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
