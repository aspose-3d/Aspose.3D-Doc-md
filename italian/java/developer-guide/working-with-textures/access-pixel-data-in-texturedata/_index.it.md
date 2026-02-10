---
title: Accesso ai dati dei pixel in TextureData
type: docs
weight: 7
url: /it/java/access-pixel-data-in-texturedata
description: Leggi o scrivi i dati dei pixel in TextureData
---
{{% alert color="primary" %}}

Questo è supportato dalla versione 23,4 o maggiore.

{{% /alert %}}



##  **Scrivi dati pixel**

Utilizzare la seguente classe per definire codificatori texture e decodificatore texture:


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

##  **Trasforma il formato pixel**

Con transformPixelFormat puoi facilmente modificare il formato pixel della texture:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
