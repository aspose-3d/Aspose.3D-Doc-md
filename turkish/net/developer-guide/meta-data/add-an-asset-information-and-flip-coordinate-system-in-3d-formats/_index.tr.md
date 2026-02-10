---
title: Sahne için bir varlık bilgisi ekleyin
type: docs
weight: 10
url: /tr/net/add-an-asset-information-to-scene
description: Meta veriler, bilgi kaynağını açıklayan, açıklayan, açıklayan veya daha kolay hale getiren, kullanan veya yöneten yapılandırılmış bilgilerdir. Aspose.3D for .NET API, geliştiricilerin sahne için bir meta veri tanımlamasına izin verir.
---
##  **3D sahnesine bir varlık bilgisi ekleyin**
Meta veriler, bilgi kaynağını açıklayan, açıklayan, açıklayan veya daha kolay hale getiren, kullanan veya yöneten yapılandırılmış bilgilerdir. Aspose.3D for .NET API, geliştiricilerin sahne için bir meta veri tanımlamasına izin verir.
###  **Define sahne için bir Metadata**
3D, büyük miktarlarda meta veri ve resim bilgisi ürettiğini gösterir. Metadata bir varlıktır ve gösterinin bir parçasıdır.

1. [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıfı kullanarak 3D sahnesini başlatın.
1. Set uygulama/araç adı.
1. Set uygulama/araç satıcı adı.
1. Set ölçüm birimi.
1. Set ölçüm birimi ölçek faktörü.
1. Save 3D scene in the supported file format.

In this example, we assume the scene is created by a CAD tool called “Egypt” and it’s designed by “Manualdesk”:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a 3D scene
Scene scene = new Scene();

// Set application/tool name
scene.AssetInfo.ApplicationName = "Egypt";

// Set application/tool vendor name
scene.AssetInfo.ApplicationVendor = "Manualdesk";

// We use ancient egyption measurement unit Pole
scene.AssetInfo.UnitName = "pole";

// One Pole equals to 60cm
scene.AssetInfo.UnitScaleFactor = 0.6;

// Save scene to 3D supported file formats
scene.Save("InformationToScene.fbx");

{{< /highlight >}}
