---
title: Импортировать 3D Сцены и Содержание из PDF в C#
linktitle: Импорт 3D Сцен и Контентов из PDF
type: docs
weight: 50
url: /ru/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Класс Сцена Aspose.3D API представляет собой сцену 3D. Разработчики могут извлекать сцены и содержимое 3D из файла PDF.
---
{{% alert color="primary" %}}

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) из Aspose.3D API представляет сцену 3D. Разработчики могут извлекать сцены и содержимое 3D из файла PDF.

{{% /alert %}}
##  **Открыть сцену из защищенного паролем PDF**
Метод `Open` класса `Scene` позволяет загрузить сцену 3D из входного файла PDF. Разработчики также могут применять пароль для защищенных PDF-файлов, используя класс [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions), как показано в этом примере кода C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **Извлеките все необработанное содержимое 3D из PDF**
Метод Extract класса [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) позволяет извлечь содержимое 3D из файла PDF. Разработчики могут перебирать содержимое и сохранять его в отдельные файлы, как показано в этом примере кода C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **Извлеките все сцены 3D и сохраните их в поддерживаемых форматах 3D**
Метод `ExtractScene` класса `PdfFormat` позволяет извлекать сцены 3D из файла PDF. Разработчики могут перебирать сцены и сохранять их в поддерживаемых форматах файлов 3D, как показано в этом примере кода C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

Все поддерживаемые форматы файлов 3D перечислены на странице [Обзор продукта](/3d/ru/net/product-overview/).

{{% /alert %}}
