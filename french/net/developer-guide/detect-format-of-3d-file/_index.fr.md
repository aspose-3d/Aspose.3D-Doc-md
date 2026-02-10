---
title: Détecter le format du fichier 3D dans C# .NET
linktitle: Détecter le format du fichier 3D
type: docs
weight: 10
url: /fr/net/detect-format-of-3d-file/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent détecter le format des fichiers 3D pris en charge dans C# avant de l'ouvrir car l'extension du fichier ne garantit pas que le contenu du fichier est approprié.
---
{{% alert color="primary" %}} 

En utilisant Aspose.3D for .NET API, les développeurs peuvent détecter le format des fichiers 3D pris en charge dans C# avant de l'ouvrir car l'extension du fichier ne garantit pas que le contenu du fichier est approprié.

{{% /alert %}} 
##  **Détecter l'échantillon de programmation de format**
L'exemple de code C# suivant illustre comment détecter un format de fichier de fichier 3D (en utilisant le chemin du fichier ou le flux) et vérifier son extension.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
