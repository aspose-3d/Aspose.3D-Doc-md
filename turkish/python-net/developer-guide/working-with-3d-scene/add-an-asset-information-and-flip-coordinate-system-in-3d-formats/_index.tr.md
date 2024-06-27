---
title: Bir varlık bilgisi ekleyin ve koordinat sistemini 3D formatlarında çevirin
type: docs
weight: 10
url: /tr/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Meta veriler, bilgi kaynağını açıklayan, açıklayan, açıklayan veya daha kolay hale getiren, kullanan veya yöneten yapılandırılmış bilgilerdir. Aspose.3D for Python via .NET API, geliştiricilerin sahne için bir meta veri tanımlamasına izin verir.
---
##  **3D sahnesine bir varlık bilgisi ekleyin**
Meta veriler, bilgi kaynağını açıklayan, açıklayan, açıklayan veya daha kolay hale getiren, kullanan veya yöneten yapılandırılmış bilgilerdir. Aspose.3D for Python via .NET API, geliştiricilerin sahne için bir meta veri tanımlamasına izin verir.
###  **Define sahne için bir Metadata**
3D, büyük miktarlarda meta veri ve resim bilgisi ürettiğini gösterir. Metadata bir varlıktır ve gösterinin bir parçasıdır.

1. `Scene` sınıfı kullanarak 3D sahnesini başlatın.
1. Set uygulama/araç adı.
1. Set uygulama/araç satıcı adı.
1. Set ölçüm birimi.
1. Set ölçüm birimi ölçek faktörü.
1. Save 3D scene in the supported file format.

In this example, we assume the scene is created by a CAD tool called “Egypt” and it’s designed by “Manualdesk”:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
##  **Koordinat sistemini 3D formatlarında çevir**
Aspose.3D for Python via .NET API allows users to flip coordinate system in the OBJ, 3DS, STL and U3D formats.

{{% alert color="primary" %}} 

Bir 3ds dosyasını içe aktarmak ve OBJ formatında kaydetmek için [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıfı kodda kullanılıyor.

{{% /alert %}} 

In this example, we flipped the coordinate system while importing the 3ds file, and saved it in OBJ format without materials.
