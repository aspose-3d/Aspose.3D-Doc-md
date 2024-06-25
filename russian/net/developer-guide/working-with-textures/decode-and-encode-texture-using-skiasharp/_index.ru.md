---
title: Декодирование и кодирование текстур с помощью SkiaSharp
type: docs
weight: 9
url: /ru/net/decode-and-encode-texture-using-skiasharp
description: Декодирование текстур из файлов изображений с помощью SkiaSharp
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики используют внешний кодировщик и декодеры изображений для загрузки текстур или сохранения текстур в различных форматах изображений.

{{% /alert %}}


##  **Используйте следующий код для определения текстурного кодека из SkiaSharp**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **Зарегистрируйте в Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


Когда этот кодек зарегистрирован, все поддерживаемые SkiaSharp форматы изображений могут быть использованы в TextureData.Save.





