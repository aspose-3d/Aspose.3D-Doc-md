---
title: Metin verilerine piksel verilerine erişin
type: docs
weight: 7
url: /tr/net/access-pixel-data-in-texturedata
description: Metin verilerinde piksel verilerini oku veya yaz
---
{{% alert color="primary" %}}

Bu sürüm 23.4 veya daha büyük tarafından desteklenmektedir.

{{% /alert %}}



##  **Piksel verileri yaz**

Doku kodlayıcıları ve doku kod çözücüsünü tanımlamak için aşağıdaki sınıfı kullanın:


{{< highlight "csharp" >}}
var tex = new TextureData(128, 128, PixelFormat.A8R8G8B8);
using (var mapping = tex.MapPixels(PixelMapMode.WriteOnly))
{
    var pixels = mapping.Data;
    var p = 0;
    for(var y = 0; y < 128; y++)
    {
        for (var x = 0; x < 128; x++)
        {
            pixels[p + 0] = 255;//alpha
            pixels[p + 1] = 255;//red
            pixels[p + 2] = 0;//green
            pixels[p + 3] = 0;//blue
            p += 4;//next pixel
        }
    }
}
tex.Save("red.png");//save to png file(Need codec registered)

{{< /highlight >}}

##  **Piksel formatını değiştir**

Transformpixelformat ile doku piksel formatını kolayca değiştirebilirsiniz:

{{< highlight "csharp" >}}
var tex = TextureData.FromFile("test.png");
tex.TransformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
