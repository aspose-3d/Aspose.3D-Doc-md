---
title: Доступ к пиксельным данным в TextureData
type: docs
weight: 7
url: /ru/java/access-pixel-data-in-texturedata
description: Чтение или запись пиксельных данных в TextureData
---
{{% alert color="primary" %}}

Это поддерживается в версии 23,4 или выше.

{{% /alert %}}



##  **Запись пиксельных данных**

Используйте следующий класс для определения кодировщиков текстур и декодеров текстур:


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

##  **Преобразование формата пикселей**

С помощью transformPixelFormat вы можете легко изменить формат пикселей текстуры:

{{< highlight "java" >}}
var tex = TextureData.fromFile("test.png");
tex.transformPixelFormat(PixelFormat.G8);//now the texture data only contains green channel in pixel.

{{< /highlight >}}
