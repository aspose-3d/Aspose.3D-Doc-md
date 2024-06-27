---
title: 3D mesh kodlaması Google Draco dosyasında
type: docs
weight: 60
url: /tr/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API geliştiricilerin bir 3D modelini içe aktarmasına ve daha sonra Google Draco dosyalarında mesh'leri kodlamasına izin verir. Geliştiriciler ayrıca bir örgü kodlamadan önce pozisyonu, doku koordinatlarını, rengi ve normal bitlerini ve sıkıştırma seviyesini de belirtebilirler.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API allows developers to [import a 3D model](/3d/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.

{{% /alert %}}
##  **3D mesh alın ve Google Draco dosyasında kodlayın**
[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) sınıfı tarafından maruz kalan `Encode` yöntemi, Google Draco dosyasında bir 3d mesh kodlamak için kullanılabilir. Parametreler olarak [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) ve [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) nesneleri alır. Draco kaydetme seçeneklerini kullanarak, geliştiriciler bir ağ kodlamadan önce konumu, doku koordinatlarını, rengini ve normal bitlerini ve sıkıştırma seviyesini de belirtebilirler.
###  **Programming ample ample**
This code example retrieves a `Mesh` of `Sphere`, and then encode in the Google Draco file after specifying a compression level.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.cs" >}}
