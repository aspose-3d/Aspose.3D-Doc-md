---
title: Metin verilerine piksel verilerine erişin
type: docs
weight: 7
url: /tr/java/access-pixel-data-in-texturedata
description: Metin verilerinde piksel verilerini oku veya yaz
---
{{% alert color="primary" %}}

Bu sürüm 23.4 veya daha büyük tarafından desteklenmektedir.

{{% /alert %}}



##  **Piksel verileri yaz**

Doku kodlayıcıları ve doku kod çözücüsünü tanımlamak için aşağıdaki sınıfı kullanın:


{{< highlight "java" >}}
TextureData tex = new TextureData(128, 128, PixelFormat.A8R8G8B8);
try (PixelMapping mapping = tex.mapPixels(PixelMapMode.WRITE_ONLY))
{
    var pixels = mapping.getData();
    var p = 0;
    for(var y = 0; y < 128; y++)
    {
        for (var x = 0; x < 128; x++)
        {
            pixels[p + 0] = (byte)255;//alpha
            pixels[p + 1] = (byte)255;//red
            pixels[p + 2] = 0;//green
            pixels[p + 3] = 0;//blue
            p += 4;//next pixel
        }
    }
}
tex.save("red.png");

{{< /highlight >}}

##  **Piksel formatını değiştir**

Transformpixelformat ile doku piksel formatını kolayca değiştirebilirsiniz:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
