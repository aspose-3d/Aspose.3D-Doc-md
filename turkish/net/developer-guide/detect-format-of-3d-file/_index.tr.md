---
title: 3D dosyasının biçimini C# .NET olarak algılayın
linktitle: 3D dosyasının biçimini algılama
type: docs
weight: 10
url: /tr/net/detect-format-of-3d-file/
description: Using Aspose.3D for .NET API, developers may detect the format of supported 3D files in C# before opening it because the file extension does not guarantee that the file content is appropriate.
---
{{% alert color="primary" %}} 

Using Aspose.3D for .NET API, developers may detect the format of supported 3D files in C# before opening it because the file extension does not guarantee that the file content is appropriate.

{{% /alert %}} 
##  **Detect Format rorogramming ample ample**
Aşağıdaki C# örnek kodu, 3D dosyasının dosya biçimini (dosya yolunu veya akışını kullanarak) nasıl tespit edeceğinizi ve uzantısını kontrol edeceğinizi gösterir.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
