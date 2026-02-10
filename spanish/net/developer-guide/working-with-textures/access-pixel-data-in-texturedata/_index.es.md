---
title: Acceder a datos de píxeles en TextureData
type: docs
weight: 7
url: /es/net/access-pixel-data-in-texturedata
description: Leer o escribir datos de píxeles en TextureData
---
{{% alert color="primary" %}}

Esto es compatible con la versión 23,4 o superior.

{{% /alert %}}



##  **Escribir datos de píxeles**

Utilice la siguiente clase para definir los codificadores de textura y el decodificador de textura:


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

##  **Transformar formato de píxel**

Con TransformPixelFormat puedes cambiar fácilmente el formato de píxeles de la textura:

{{< highlight "csharp" >}}
var tex = TextureData.FromFile("test.png");
tex.TransformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
