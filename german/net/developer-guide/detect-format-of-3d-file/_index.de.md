---
title: Erkennen Sie das Format der 3D-Datei in C# .NET
linktitle: Erkennen Sie das Format der 3D-Datei
type: docs
weight: 10
url: /de/net/detect-format-of-3d-file/
description: Mit Aspose.3D for .NET API können Entwickler das Format der unterstützten 3D-Dateien in C# erkennen, bevor sie sie öffnen, da die Datei erweiterung nicht garantiert, dass der Datei inhalt geeignet ist.
---
{{% alert color="primary" %}} 

Mit Aspose.3D for .NET API können Entwickler das Format der unterstützten 3D-Dateien in C# erkennen, bevor sie sie öffnen, da die Datei erweiterung nicht garantiert, dass der Datei inhalt geeignet ist.

{{% /alert %}} 
##  **Muster für die Format programmierung erkennen**
Der folgende C# Beispielcode ver anschaulicht, wie Sie ein Dateiformat von 3D-Datei (unter Verwendung des Datei pfads oder-Streams) erkennen und die Erweiterung überprüfen.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
