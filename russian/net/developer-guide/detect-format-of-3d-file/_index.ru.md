---
title: Определение формата файла 3D в C# .NET
linktitle: Определение формата файла 3D
type: docs
weight: 10
url: /ru/net/detect-format-of-3d-file/
description: Используя Aspose.3D for .NET API, разработчики могут определить формат поддерживаемых файлов 3D в C# перед его открытием, поскольку расширение файла не гарантирует, что содержимое файла подходит.
---
{{% alert color="primary" %}} 

Используя Aspose.3D for .NET API, разработчики могут определить формат поддерживаемых файлов 3D в C# перед его открытием, поскольку расширение файла не гарантирует, что содержимое файла подходит.

{{% /alert %}} 
##  **Обнаружить образец программирования формата**
Следующий пример C# показывает, как определить формат файла 3D (используя путь к файлу или поток) и проверить его расширение.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
