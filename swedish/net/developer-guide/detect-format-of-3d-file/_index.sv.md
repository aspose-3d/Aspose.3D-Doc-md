---
title: Upptäck format för 3D-fil i C# .NET
linktitle: Upptäck format för 3D-filen
type: docs
weight: 10
url: /sv/net/detect-format-of-3d-file/
description: Använder Aspose. 3D for .NET API, utvecklare kan upptäcka formatet för stödda 3D filer i C# innan den öppnas eftersom filändelsen inte garanterar att filens innehåll inte garanterar t är lämpligt.
---
{{% alert color="primary" %}} 

Använder Aspose. 3D for .NET API, utvecklare kan upptäcka formatet för stödda 3D filer i C# innan den öppnas eftersom filändelsen inte garanterar att filens innehåll inte garanterar t är lämpligt.

{{% /alert %}} 
##  **Detektera formatprogrammeringsprover**
Följande C# sample- kod illustrerar hur filformatet ska detekteras med 3D filen (med filsökvägen eller strömmen) och kontrollera dess förlängning.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
