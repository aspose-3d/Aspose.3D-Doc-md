---
title: Add Asset Information to 3D document
type: docs
weight: 10
url: /tr/java/add-asset-information-to-3d-document/
description: Meta veriler, bilgi kaynağını açıklayan, açıklayan, açıklayan veya daha kolay hale getiren, kullanan veya yöneten yapılandırılmış bilgilerdir. Aspose.3D for Java API sahne için meta verileri tanımlamak için desteğe sahiptir.
---
##  **Add Asset Information to 3D document**
Meta veriler, bilgi kaynağını açıklayan, açıklayan, açıklayan veya daha kolay hale getiren, kullanan veya yöneten yapılandırılmış bilgilerdir. Aspose.3D for Java API sahne için meta verileri tanımlamak için desteğe sahiptir.
###  **Define sahne için bir Metadata**
3D, büyük miktarlarda meta veri ve resim bilgisi ürettiğini gösterir. Metadata bir varlıktır ve gösterinin bir parçasıdır.

1. `Scene` sınıfı kullanarak 3D sahnesini başlatın.
1. Set uygulama/araç adı.
1. Set uygulama/araç satıcı adı.
1. Set ölçüm birimi.
1. Set ölçüm birimi ölçek faktörü.
1. Save 3D scene in the supported file format.

In this example, we assume the scene is created by a CAD tool called “Egypt” and it’s designed by “Manualdesk”:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
