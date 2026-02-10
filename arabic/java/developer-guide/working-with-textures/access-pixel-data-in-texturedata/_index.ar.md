---
title: وصول بيانات البكسل في TextureData
type: docs
weight: 7
url: /ar/java/access-pixel-data-in-texturedata
description: قراءة أو كتابة بيانات البكسل في TextureData
---
{{% alert color="primary" %}}

هذا مدعوم بالإصدار 23.4 أو أكبر.

{{% /alert %}}



##  **كتابة بيانات البكسل**

استخدم الفئة التالية لتحديد مشفرات النسيج وفك تشفيره:


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

##  **تحويل تنسيق البكسل**

مع transformPixelFormat يمكنك بسهولة تغيير تنسيق البكسل للنسيج:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
