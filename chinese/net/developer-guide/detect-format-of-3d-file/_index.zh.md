---
title: 检测 C# .NET 中 3D 文件的格式
linktitle: 检测 3D 文件的格式
type: docs
weight: 10
url: /zh/net/detect-format-of-3d-file/
description: 使用 Aspose.3D for .NET API，开发人员可能会在打开 C# 中受支持的 3D 文件的格式之前检测到它，因为文件扩展名不能保证文件内容是适当的。
---
{{% alert color="primary" %}} 

使用 Aspose.3D for .NET API，开发人员可能会在打开 C# 中受支持的 3D 文件的格式之前检测到它，因为文件扩展名不能保证文件内容是适当的。

{{% /alert %}} 
##  **检测格式编程示例**
以下 C# 示例代码说明如何检测 3D 文件的文件格式 (使用文件路径或流) 并检查其扩展名。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
