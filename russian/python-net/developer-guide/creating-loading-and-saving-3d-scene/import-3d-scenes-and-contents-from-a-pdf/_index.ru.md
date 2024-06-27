---
title: Импорт 3D Сцен и Контентов из PDF
type: docs
weight: 50
url: /ru/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: Класс Сцена Aspose.3D API представляет собой сцену 3D. Разработчики могут извлекать сцены и содержимое 3D из файла PDF.
---
{{% alert color="primary" %}}

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) из Aspose.3D API представляет сцену 3D. Разработчики могут извлекать сцены и содержимое 3D из файла PDF.

{{% /alert %}}
##  **Открыть сцену из защищенного паролем PDF**
Метод `open` класса `Scene` позволяет загрузить сцену 3D из входного файла PDF. Разработчики также могут применять пароль для защищенных PDF-файлов, используя класс [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions), как показано в этом примере кода:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
##  **Извлеките все необработанное содержимое 3D из PDF**
Метод `extract` класса [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) позволяет извлечь содержимое 3D из файла PDF. Разработчики могут перебирать содержимое и сохранять его в отдельные файлы, как показано в этом примере кода:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
##  **Извлеките все сцены 3D и сохраните их в поддерживаемых форматах 3D**
Метод `extract_scene` класса `PdfFormat` позволяет извлекать сцены 3D из файла PDF. Разработчики могут выполнять итерации по сценам и сохранять их в поддерживаемых форматах файлов 3D, как показано в этом примере кода:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Все поддерживаемые форматы файлов 3D перечислены на странице [Обзор продукта](/3d/ru/python-net/product-overview/).

{{% /alert %}}
