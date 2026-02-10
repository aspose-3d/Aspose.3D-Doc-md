---
title: 访问TextureData中的像素数据
type: docs
weight: 7
url: /zh/net/access-pixel-data-in-texturedata
description: 在TextureData中读取或写入像素数据
---
{{% alert color="primary" %}}

版本23.4或更高版本支持此功能。

{{% /alert %}}



##  **写入像素数据**

使用以下类定义纹理编码器和纹理解码器:


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

##  **变换像素格式**

使用TransformPixelFormat，您可以轻松更改纹理的像素格式:

{{< highlight "csharp" >}}
var tex = TextureData.FromFile("test.png");
tex.TransformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
