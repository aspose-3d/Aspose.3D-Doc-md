---
title: Detect format of 3D file in C# .NET
linktitle: Detect format of 3D file
type: docs
weight: 10
url: /net/detect-format-of-3d-file/
description: Using Aspose.3D for .NET API, developers may detect the format of supported 3D files in C# before opening it because the file extension does not guarantee that the file content is appropriate.
---

{{% alert color="primary" %}} 

Using Aspose.3D for .NET API, developers may detect the format of supported 3D files in C# before opening it because the file extension does not guarantee that the file content is appropriate.

{{% /alert %}} 
## **Detect Format Programming Sample**
The following C# sample code illustrates how to detect a file format of 3D file (using the file path or stream) and check its extension.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
