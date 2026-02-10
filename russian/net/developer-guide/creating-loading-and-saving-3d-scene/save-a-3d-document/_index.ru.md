---
title: Сохраните документ 3D в разных форматах 3D, используя C#
linktitle: Сохраните документ 3D
type: docs
weight: 20
url: /ru/net/save-a-3d-document/
description: Класс Сцена Aspose.3D API представляет собой документ 3D, и разработчики могут сохранить его объект в любом поддерживаемом формате файла.
---
##  **Обзор**
В статье объясняется, как можно сохранить документ 3D в различных форматах, используя библиотеку обработки документов C# 3D, включая

- Сохраните документ 3D в формате FBX, используя C# - AutoDesk
- Сохраните документ 3D в формате DAE, используя C# - Collada
- Сохраните документ 3D в формате 3DS, используя C# - Discreet 3D Studio
- Сохраните документ 3D в формате DRC, используя C# - Google Draco

{{% alert color="primary" %}} 

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) Aspose.3D API представляет собой документ 3D, и разработчики могут сохранить его объект в любом поддерживаемом формате файла. Чтобы сохранить сцену 3D, просто используйте метод [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), он принимает имя файла с полным путем или объект потока файлов. Aspose.3D API предлагает еще один параметр `FileFormat` для указания формата выходного файла.

{{% /alert %}} 

##  **Сохраните сцену 3D в поддерживаемых форматах 3D**

Пример кода C# ниже показывает, как сохранить сцену или документ 3D в потоке в различных поддерживаемых форматах 3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
