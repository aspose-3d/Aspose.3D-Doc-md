---
title: Accesso ai dati dei pixel in TextureData
type: docs
weight: 7
url: /it/net/access-pixel-data-in-texturedata
description: Leggi o scrivi i dati dei pixel in TextureData
---
{{% alert color="primary" %}}

Questo è supportato dalla versione 23,4 o maggiore.

{{% /alert %}}



##  **Scrivi dati pixel**

Utilizzare la seguente classe per definire codificatori texture e decodificatore texture:


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

##  **Trasforma il formato pixel**

Con TransformPixelFormat puoi cambiare facilmente il formato pixel della texture:

{{< highlight "csharp" >}}
var tex = TextureData.FromFile("test.png");
tex.TransformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
