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

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Koordinat sistemini 3D formatlarında çevir**
Aspose.3D for Python via .NET API allows users to flip coordinate system in the OBJ, 3DS, STL and U3D formats.

{{% alert color="primary" %}} 

Bir 3ds dosyasını içe aktarmak ve OBJ formatında kaydetmek için [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıfı kodda kullanılıyor.

{{% /alert %}} 

In this example, we flipped the coordinate system while importing the 3ds file, and saved it in OBJ format without materials.
