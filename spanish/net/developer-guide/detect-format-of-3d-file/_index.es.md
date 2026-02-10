---
title: Detectar el formato del archivo 3D en C# .NET
linktitle: Detectar formato de archivo 3D
type: docs
weight: 10
url: /es/net/detect-format-of-3d-file/
description: Al usar Aspose.3D for .NET API, los desarrolladores pueden detectar el formato de los archivos 3D compatibles en C# antes de abrirlo porque la extensión del archivo no garantiza que el contenido del archivo sea apropiado.
---
{{% alert color="primary" %}} 

Al usar Aspose.3D for .NET API, los desarrolladores pueden detectar el formato de los archivos 3D compatibles en C# antes de abrirlo porque la extensión del archivo no garantiza que el contenido del archivo sea apropiado.

{{% /alert %}} 
##  **Detectar formato de muestra de programación**
El siguiente código de ejemplo C# ilustra cómo detectar un formato de archivo 3D (utilizando la ruta de acceso o secuencia del archivo) y comprobar su extensión.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
