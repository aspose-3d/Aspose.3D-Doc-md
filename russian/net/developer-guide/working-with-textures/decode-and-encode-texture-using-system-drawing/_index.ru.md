---
title: Декодирование и кодирование текстуры с помощью System.Drawing
type: docs
weight: 7
url: /ru/net/decode-and-encode-texture-using-system-drawing
description: Декодирование текстуры из файлов изображений с помощью System.Drawing
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики используют внешний кодировщик и декодеры изображений для загрузки текстур или сохранения текстур в различных форматах изображений.

{{% /alert %}}

##  **Реализовать текстурный кодек с помощью System.Drawing**

Используйте следующий класс для определения кодировщиков текстур и декодеров текстур:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **Зарегистрируйте в Aspose.3D**

Теперь давайте зарегистрируем его в Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


Когда этот кодек зарегистрирован, все форматы изображений, поддерживаемые System.Drawing, могут быть использованы в TextureData.Save.

