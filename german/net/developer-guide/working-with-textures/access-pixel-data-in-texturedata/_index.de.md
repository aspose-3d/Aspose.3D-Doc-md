---
title: Zugriff auf Pixel daten in Texture Data
type: docs
weight: 7
url: /de/net/access-pixel-data-in-texturedata
description: Lesen oder Schreiben von Pixel daten in Texture Data
---
{{% alert color="primary" %}}

Dies wird von Version 23.4 oder höher unterstützt.

{{% /alert %}}



##  **Schreiben Sie Pixel daten**

Verwenden Sie die folgende Klasse, um Textur-Encoder und Textur-Decoder zu definieren:


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

##  **Pixel format transformieren**

Mit Transform Pixel Format können Sie das Pixel format der Textur leicht ändern:

{{< highlight "csharp" >}}
var tex = TextureData.FromFile("test.png");
tex.TransformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
