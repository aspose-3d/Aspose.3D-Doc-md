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

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import PdfLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a new scene
scene = Scene()
options = PdfLoadOptions()
options.password = "password".encode("utf-8")
#  Use loading options and apply password
opt = options
#  Open scene
scene.open("data-dir"  + "House_Design.pdf", opt)

{{< /highlight >}}
##  **Извлеките все необработанное содержимое 3D из PDF**
Метод `extract` класса [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) позволяет извлечь содержимое 3D из файла PDF. Разработчики могут перебирать содержимое и сохранять его в отдельные файлы, как показано в этом примере кода:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
password = None
#  Extract 3D contents
contents = FileFormat.PDF.extract("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the contents and in separate 3D files
for content in contents:
    fileName = "3d-"  + str(i)
    i = i + 1
    with open(fileName, "wb") as f:
        f.write(content)

{{< /highlight >}}
##  **Извлеките все сцены 3D и сохраните их в поддерживаемых форматах 3D**
Метод `extract_scene` класса `PdfFormat` позволяет извлекать сцены 3D из файла PDF. Разработчики могут выполнять итерации по сценам и сохранять их в поддерживаемых форматах файлов 3D, как показано в этом примере кода:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
password = None
scenes = FileFormat.PDF.extract_scene("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the scenes and save in 3D files
for scene in scenes:
    fileName = "3d-"  + str(i) + ".fbx"
    i = i + 1
    scene.save("out"  + fileName, FileFormat.FBX7400ASCII)

{{< /highlight >}}

{{% alert color="primary" %}}

Все поддерживаемые форматы файлов 3D перечислены на странице [Обзор продукта](/3d/ru/python-net/product-overview/).

{{% /alert %}}
