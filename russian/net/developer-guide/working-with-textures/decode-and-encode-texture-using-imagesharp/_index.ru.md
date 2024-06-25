---
title: Декодирование и кодирование текстур с помощью ImageSharp
type: docs
weight: 11
url: /ru/net/decode-and-encode-texture-using-imagesharp
description: Декодирование текстур из файлов изображений с помощью ImageSharp
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики используют внешний кодировщик и декодеры изображений для загрузки текстур или сохранения текстур в различных форматах изображений.

{{% /alert %}}

##  **Реализовать текстурный кодек с помощью ImageSharp**

Используйте следующий класс для определения кодировщиков текстур и декодеров текстур:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


##  **Зарегистрируйте в Aspose.3D**

Теперь давайте зарегистрируем его в Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{< /highlight >}}


Когда этот кодек зарегистрирован, все поддерживаемые ImageSharp форматы изображений могут быть использованы в TextureData.Save.

