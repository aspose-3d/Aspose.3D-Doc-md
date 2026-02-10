---
title: 访问TextureData中的像素数据
type: docs
weight: 7
url: /zh/java/access-pixel-data-in-texturedata
description: 在TextureData中读取或写入像素数据
---
{{% alert color="primary" %}}

版本23.4或更高版本支持此功能。

{{% /alert %}}



##  **写入像素数据**

使用以下类定义纹理编码器和纹理解码器:


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

##  **变换像素格式**

使用transformPixelFormat，您可以轻松更改纹理的像素格式:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
