---
title: Accéder aux données de pixel dans TextureData
type: docs
weight: 7
url: /fr/java/access-pixel-data-in-texturedata
description: Lire ou écrire des données de pixel dans TextureData
---
{{% alert color="primary" %}}

Ceci est pris en charge par la version 23.4 ou supérieure.

{{% /alert %}}



##  **Écrire des données de pixel**

Utilisez la classe suivante pour définir les encodeurs de texture et le décodeur de texture:


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

##  **Transformer le format de pixel**

Avec transformPixelFormat, vous pouvez facilement changer le format de pixel de la texture:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
