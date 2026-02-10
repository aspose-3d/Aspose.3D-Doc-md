---
title: Сохраните сцену 3D в PDF в C#
linktitle: Сохраните сцену 3D в PDF
type: docs
weight: 60
url: /ru/net/save-a-3d-scene-in-the-pdf/
description: Класс Сцена Aspose.3D API представляет собой сцену 3D. Разработчики могут построить сцену 3D, добавив камеру, свет, многоугольники и различные другие объекты. Теперь они также могут сохранить сцену 3D в формате PDF.
---
##  **Обзор**

В этой статье объясняется, как можно конвертировать файл 3D в формат PDF, используя манипуляции с файлом C# .NET 3D и конвертирование API, сначала нужно [Загрузить файл 3D в объект Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/), а затем сохранить его в формате PDF. Он охватывает широкий круг тем, например

- Конвертировать 3D в PDF в C#
- Конвертировать FBX в PDF в C#
- Конвертировать STL в PDF в C#
- Конвертировать U3D в PDF в C#
- Конвертировать OBJ в PDF в C#

{{% alert color="primary" %}} 

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) из Aspose.3D API представляет сцену 3D. Разработчики могут построить сцену 3D, добавив камеру, свет, многоугольники и различные другие объекты. Теперь они также могут сохранить сцену 3D в формате PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET напрямую записывает информацию о API и номере версии в выходные документы. Например, при рендеринге чертежа PDF, Aspose.3D for .NET заполняет поле `Application` значением 'Aspose.3D' и `PDF Producer` поля со значением e.g 'Aspose.3D 17,9'.

Обратите внимание, что вы не можете указать Aspose.3D for .NET API изменить или удалить эту информацию из выходных документов.

{{% /alert %}} 
##  **Создать 3D PDF с цилиндром и отобразить в режиме затененной иллюстрации с оптимизированным освещением CAD**
Метод Save класса `Scene` позволяет сохранить сцену 3D в формате PDF. Разработчики могут загрузить любой поддерживаемый 3D файл или построить новую 3D сцену, они могут сохранить 3D сцену в формате PDF, как показано в этом примере кода C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a new scene
            Scene scene = new Scene();
            // Create a cylinder child node
            scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan) };
            // Set rendering mode and lighting scheme
            PdfSaveOptions opt = new PdfSaveOptions();
            opt.LightingScheme = PdfLightingScheme.CAD;
            opt.RenderMode = PdfRenderMode.ShadedIllustration;
            // Save in the PDF format
            scene.Save("output_out.pdf", opt);

{{< /highlight >}}
