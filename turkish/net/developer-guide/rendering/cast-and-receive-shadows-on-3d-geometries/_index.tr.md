---
title: Cast and Receive Shadows on 3D Geometries
type: docs
weight: 10
url: /tr/net/cast-and-receive-shadows-on-3d-geometries/
description: Generally, some 3D file formats can store shadow related settings in geometry like FBX. Using Aspose.3D for .NET, developers can render an image by mapping shadows from the viewpoint of a light source. The image quality depends on the light source, elevation angle and distance between the camera and geometric objects.
---
{{% alert color="primary" %}}

Generally, some 3D file formats can store shadow related settings in geometry like FBX. Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can render an image by mapping shadows from the viewpoint of a light source. The image quality depends on the light source, elevation angle and distance between the camera and geometric objects.

{{% /alert %}}
##  **Cast ve Reeve Shadow**
Varsayılan olarak, sahnedeki tüm nesneler bir ışık kaynağından gölgeler döküyor. Developers, nesne yüzeyinde nesne bazında da gölgeler alabilir. Tkod örneği, ışık ve kamera nesnelerinin konumunu nasıl ayarlayacağını gösterir. It ayrıca bir uçak oluşturur ve farklı renkler ve gölge ayarları ile üç nesne yerleştirir.

All geometries has `CastShadows = true` and `ReceiveShadows=true`, the shadows of red box and torus casted to the plane, the red box won't receive shadows and blue box won't cast shadows.
###  **Programming ample ample**
This code example casts and Receives shadows on 3D geometries.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Render esuesult**

! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
