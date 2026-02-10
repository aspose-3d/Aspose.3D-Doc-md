---
title: Access pixel data in TextureData
type: docs
weight: 7
url: /java/access-pixel-data-in-texturedata
description: Read or write pixel data in TextureData
---

{{% alert color="primary" %}}

This is supported by version 23.4 or greater.

{{% /alert %}}



## **Write pixel data**

Use the following class to define texture encoders and texture decoder:


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

## **Transform pixel format**

With transformPixelFormat you can easily change the texture's pixel format:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
