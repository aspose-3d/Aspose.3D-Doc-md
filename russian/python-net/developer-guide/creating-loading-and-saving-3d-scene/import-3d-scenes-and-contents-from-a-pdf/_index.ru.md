---
title: Импорт 3D сцен и содержимого из PDF
type: docs
weight: 50
url: /ru/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: Класс сцены Aspose.3D API представляет собой сцену 3D. Разработчики могут извлечь 3D сцены и содержимое из файла PDF.
---
{{% alert color="primary" %}}

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) API представляет собой сцену 3D. Разработчики могут извлечь 3D сцены и содержимое из файла PDF.

{{% /alert %}}
## **Открытая сцена из защищенного паролем PDF**
Метод `open` класса `Scene` позволяет загружать сцену 3D из входного файла PDF. Разработчики также могут применять пароль для защищенных PDF-файлов с использованием класса [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions), как показано в этом примере кода:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
## **Выдержите все сырое содержимое 3D из PDF**
Метод `extract` класса [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) позволяет извлекать содержимое 3D из файла PDF. Разработчики могут повторять содержимое и сохранять их в отдельные файлы, как показано в этом примере кода:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
## **Извлеките все сцены 3D и сохраните их в поддерживаемые форматы 3D**
Метод `extract_scene` класса `PdfFormat` позволяет извлекать 3D сцены из файла PDF. Разработчики могут повторять сцены и сохранять их в поддерживаемых форматах файлов 3D, как показано в этом примере кода:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Все поддерживаемые форматы файлов 3D перечислены в[Обзор продукта](/3d/ru/python-net/product-overview/)Страница.

{{% /alert %}}
