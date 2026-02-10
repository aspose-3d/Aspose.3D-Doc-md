---
title: Detectar formato de archivo 3D
type: docs
weight: 10
url: /es/java/detect-format-of-3d-file/
description: Aspose.3D for Java API admite la detección de formatos compatibles con 3D antes de abrir porque la extensión del archivo no garantiza que el contenido del archivo sea apropiado.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API admite la detección de formatos compatibles con 3D antes de abrir porque la extensión del archivo no garantiza que el contenido del archivo sea apropiado.

{{% /alert %}} 
##  **Detectar formato de muestra de programación**
Este código fuente ilustra cómo detectar el formato del archivo (utilizando la ruta de acceso o flujo) y comprobar su extensión.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




