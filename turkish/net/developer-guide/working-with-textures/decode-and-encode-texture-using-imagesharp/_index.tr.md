---
title: Decode sharp kullanarak dokuyu kodlayın ve kodlayın
type: docs
weight: 11
url: /tr/net/decode-and-encode-texture-using-imagesharp
description: Imagesharp kullanarak görüntü dosyalarından doku çözme
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers use external image encoder and decoders to load textures or save textures into different image formats.

{{% /alert %}}

##  **Imagesharp kullanarak bir doku kodek uygulamak**

Doku kodlayıcıları ve doku kod çözücüsünü tanımlamak için aşağıdaki sınıfı kullanın:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


##  **Aspose 'a kaydedin. 3D**

Şimdi aspsoe. 3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{< /highlight >}}


Bu kodek kaydedildiğinde, tüm imagesharp desteklenen görüntü biçimleri metin verilerinde kullanılabilir. kaydet.

