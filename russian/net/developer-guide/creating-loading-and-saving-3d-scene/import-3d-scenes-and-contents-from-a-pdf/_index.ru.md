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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Извлеките все необработанное содержимое 3D из PDF**
Метод Extract класса [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) позволяет извлечь содержимое 3D из файла PDF. Разработчики могут перебирать содержимое и сохранять его в отдельные файлы, как показано в этом примере кода C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
byte[] password = null;
// Extract 3D contents
List<byte[]> contents = FileFormat.PDF.Extract("House_Design.pdf", password);
int i = 1;
// Iterate through the contents and in separate 3D files
foreach (byte[] content in contents)
{
    string fileName = "3d-" + (i++);
    File.WriteAllBytes(fileName, content);
}

{{< /highlight >}}
##  **Извлеките все сцены 3D и сохраните их в поддерживаемых форматах 3D**
Метод `ExtractScene` класса `PdfFormat` позволяет извлекать сцены 3D из файла PDF. Разработчики могут перебирать сцены и сохранять их в поддерживаемых форматах файлов 3D, как показано в этом примере кода C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            byte[] password = null;
            List<Scene> scenes = FileFormat.PDF.ExtractScene("House_Design.pdf", password);
            int i = 1;
            // Iterate through the scenes and save in 3D files
            foreach (Scene scene in scenes)
            {
                string fileName = "3d-" + (i++) + ".fbx";
                scene.Save(RunExamples.GetOutputFilePath(fileName), FileFormat.FBX7400ASCII);
            }

{{< /highlight >}}

{{% alert color="primary" %}}

Все поддерживаемые форматы файлов 3D перечислены на странице [Обзор продукта](/3d/ru/net/product-overview/).

{{% /alert %}}
