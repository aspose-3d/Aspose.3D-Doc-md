---
title: 3D mesh kodlaması Google Draco dosyasında
type: docs
weight: 60
url: /tr/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API allows developers to import a 3D model, and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API allows developers to [import a 3D model](/3d/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.

{{% /alert %}}
##  **3D mesh alın ve Google Draco dosyasında kodlayın**
[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) sınıfı tarafından maruz kalan `encode` yöntemi, Google Draco dosyasında bir 3d mesh kodlamak için kullanılabilir. Parametreler olarak [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) ve [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) nesneleri alır. Draco kaydetme seçeneklerini kullanarak, geliştiriciler bir ağ kodlamadan önce konumu, doku koordinatlarını, rengini ve normal bitlerini ve sıkıştırma seviyesini de belirtebilirler.
###  **Programming ample ample**
Bu kod örneği bir küre ağı alır ve daha sonra bir sıkıştırma seviyesi belirledikten sonra Google Draco dosyasında kodlanır.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
