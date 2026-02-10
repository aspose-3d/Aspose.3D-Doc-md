---
title: Zugriff auf Pixel daten in Texture Data
type: docs
weight: 7
url: /de/java/access-pixel-data-in-texturedata
description: Lesen oder Schreiben von Pixel daten in Texture Data
---
{{% alert color="primary" %}}

Dies wird von Version 23.4 oder höher unterstützt.

{{% /alert %}}



##  **Schreiben Sie Pixel daten**

Verwenden Sie die folgende Klasse, um Textur-Encoder und Textur-Decoder zu definieren:


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

##  **Pixel format transformieren**

Mit transform Pixel Format können Sie das Pixel format der Textur leicht ändern:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
