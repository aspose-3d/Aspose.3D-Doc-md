---
title: Импорт 3D сцен и содержимого из PDF в C#
linktitle: Импорт 3D сцен и содержимого из PDF
type: docs
weight: 50
url: /ru/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Класс сцены Aspose.3D API представляет собой сцену 3D. Разработчики могут извлечь 3D сцены и содержимое из файла PDF.
---
{{% alert color="primary" %}}

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) API представляет собой сцену 3D. Разработчики могут извлечь 3D сцены и содержимое из файла PDF.

{{% /alert %}}
## **Открытая сцена из защищенного паролем PDF**
Метод `Open` класса `Scene` позволяет загружать сцену 3D из входного файла PDF. Разработчики также могут применять пароль для защищенных PDF-файлов с использованием класса [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions), как показано в этом примере кода C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
## **Выдержите все сырое содержимое 3D из PDF**
Метод Extract класса [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) позволяет извлекать содержимое 3D из файла PDF. Разработчики могут перебирать содержимое и сохранять их в отдельные файлы, как показано в этом примере кода C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
## **Извлеките все сцены 3D и сохраните их в поддерживаемые форматы 3D**
Метод `ExtractScene` класса `PdfFormat` позволяет извлекать 3D сцены из файла PDF. Разработчики могут повторять сцены и сохранять их в поддерживаемых форматах файлов 3D, как показано в этом примере кода C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

Все поддерживаемые форматы файлов 3D перечислены в[Обзор продукта](/3d/ru/net/product-overview/)Страница.

{{% /alert %}}
