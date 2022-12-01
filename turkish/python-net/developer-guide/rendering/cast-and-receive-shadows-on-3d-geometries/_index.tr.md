---
title: Cast ve Reeve hahadows 3D eoeometries üzerinde
type: docs
weight: 10
url: /tr/python-net/cast-and-receive-shadows-on-3d-geometries/
description: Generally, bazı 3D dosya biçimleri FBX gibi geometride gölge ile ilgili ayarları saklayabilir. Python via .NET için Aspose.3D sing sing, geliştiriciler bir ışık kaynağının bakış açısından gölgeleri haritalandırarak bir görüntü oluşturabilirler. The görüntü kalitesi, kamera ve geometrik nesneler arasındaki ışık kaynağına, yükseklik açısına ve mesafeye bağlıdır.
---
{{% alert color="primary" %}}

Generally, bazı 3D dosya biçimleri FBX gibi geometride gölge ile ilgili ayarları saklayabilir. Using[Python via .NET için Aspose.3D](https://products.aspose.com/3d/python-net/)Geliştiriciler, bir ışık kaynağının bakış açısından gölgeleri haritalandırarak bir görüntü oluşturabilirler. The görüntü kalitesi, kamera ve geometrik nesneler arasındaki ışık kaynağına, yükseklik açısına ve mesafeye bağlıdır.

{{% /alert %}}
## **Cast ve Reeve Shadow**
Varsayılan olarak, sahnedeki tüm nesneler bir ışık kaynağından gölgeler döküyor. Developers, nesne yüzeyinde nesne bazında da gölgeler alabilir. Tkod örneği, ışık ve kamera nesnelerinin konumunu nasıl ayarlayacağını gösterir. It ayrıca bir uçak oluşturur ve farklı renkler ve gölge ayarları ile üç nesne yerleştirir.

All geometrileri `cast_shadows = True` ve `receive_shadows = True`, kırmızı kutu ve torus gölgeleri uçağa dökülür, kırmızı kutu gölgeler almaz ve mavi kutu gölgeleri atmaz.
### **Programming ample ample**
Code kod örneği 3D geometrilerinde gölgeleri ve gölgeleri çıkarır.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Render esuesult**

![Todo: görüntü_Alt_Metin](cast-and-receive-shadows-on-3d-geometries_1.png)
