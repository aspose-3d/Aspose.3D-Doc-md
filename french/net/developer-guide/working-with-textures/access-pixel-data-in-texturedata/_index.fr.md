---
title: Accéder aux données de pixel dans TextureData
type: docs
weight: 7
url: /fr/net/access-pixel-data-in-texturedata
description: Lire ou écrire des données de pixel dans TextureData
---
{{% alert color="primary" %}}

Ceci est pris en charge par la version 23.4 ou supérieure.

{{% /alert %}}



##  **Écrire des données de pixel**

Utilisez la classe suivante pour définir les encodeurs de texture et le décodeur de texture:


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

##  **Transformer le format de pixel**

Avec TransformPixelFormat, vous pouvez facilement changer le format de pixel de la texture:

{{< highlight "csharp" >}}
var tex = TextureData.FromFile("test.png");
tex.TransformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
