---
title: Cast ve Reeve hahadows 3D eoeometries üzerinde
type: docs
weight: 10
url: /tr/net/cast-and-receive-shadows-on-3d-geometries/
description: Generally, bazı 3D dosya biçimleri FBX gibi geometride gölge ile ilgili ayarları saklayabilir. 07sing Aspose.3D for .NET, geliştiriciler bir ışık kaynağının bakış açısından gölgeleri haritalandırarak bir görüntü oluşturabilirler. The görüntü kalitesi, kamera ve geometrik nesneler arasındaki ışık kaynağına, yükseklik açısına ve mesafeye bağlıdır.
---
{{% alert color="primary" %}}

Generally, bazı 3D dosya biçimleri FBX gibi geometride gölge ile ilgili ayarları saklayabilir. Using[Aspose.3D for .NET](https://products.aspose.com/3d/net/)Geliştiriciler, bir ışık kaynağının bakış açısından gölgeleri haritalandırarak bir görüntü oluşturabilirler. The görüntü kalitesi, kamera ve geometrik nesneler arasındaki ışık kaynağına, yükseklik açısına ve mesafeye bağlıdır.

{{% /alert %}}
## **Cast ve Reeve Shadow**
Varsayılan olarak, sahnedeki tüm nesneler bir ışık kaynağından gölgeler döküyor. Developers, nesne yüzeyinde nesne bazında da gölgeler alabilir. Tkod örneği, ışık ve kamera nesnelerinin konumunu nasıl ayarlayacağını gösterir. It ayrıca bir uçak oluşturur ve farklı renkler ve gölge ayarları ile üç nesne yerleştirir.

All geometrileri `CastShadows = true` ve `ReceiveShadows=true`, kırmızı kutu ve torus gölgeleri uçağa dökülür, kırmızı kutu gölgeler almaz ve mavi kutu gölgeleri atmaz.
### **Programming ample ample**
Code kod örneği 3D geometrilerinde gölgeleri ve gölgeleri çıkarır.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Render esuesult**

![Todo: görüntü_Alt_Metin](cast-and-receive-shadows-on-3d-geometries_1.png)
