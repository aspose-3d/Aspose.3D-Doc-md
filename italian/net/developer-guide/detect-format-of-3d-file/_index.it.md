---
title: Rileva il formato del file 3D in C# .NET
linktitle: Rileva il formato del file 3D
type: docs
weight: 10
url: /it/net/detect-format-of-3d-file/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono rilevare il formato dei file 3D supportati in C# prima di aprirlo perché l'estensione del file non garantisce che il contenuto del file sia appropriato.
---
{{% alert color="primary" %}} 

Utilizzando Aspose.3D for .NET API, gli sviluppatori possono rilevare il formato dei file 3D supportati in C# prima di aprirlo perché l'estensione del file non garantisce che il contenuto del file sia appropriato.

{{% /alert %}} 
##  **Rileva il campione di programmazione del formato**
Il seguente codice di esempio C# illustra come rilevare un formato di file di 3D (utilizzando il percorso o lo streaming del file) e verificarne l'estensione.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
