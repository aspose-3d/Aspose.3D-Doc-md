---
title: Sahneyi sıkıştırılmış AMF formatına aktar
type: docs
weight: 60
url: /tr/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java, gereksinimlerinize göre sıkıştırma için boole değerini ayarlamanızı sağlayan amfsaveoptions sınıfı sunar.
---
#  **Sahneyi sıkıştırılmış AMF formatına aktar**
Aspose.3D for Node.js via Java, gereksinimlerinize göre sıkıştırma için boole değerini ayarlamanızı sağlayan `AmfSaveOptions` sınıfı sunar. Varsayılan olarak değer doğrudur. Kod parçacığı aşağıdaki sıkıştırılmış AMF format dosyası oluşturmak için tam işlevselliği gösterir:

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
