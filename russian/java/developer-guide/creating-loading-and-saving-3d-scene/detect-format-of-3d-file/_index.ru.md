---
title: Определение формата файла 3D
type: docs
weight: 10
url: /ru/java/detect-format-of-3d-file/
description: Aspose.3D for Java API поддерживает определение поддерживаемых форматов 3D перед открытием, поскольку расширение файла не гарантирует, что содержимое файла подходит.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API поддерживает определение поддерживаемых форматов 3D перед открытием, поскольку расширение файла не гарантирует, что содержимое файла подходит.

{{% /alert %}} 
##  **Обнаружить образец программирования формата**
Этот исходный код иллюстрирует, как обнаружить формат файла (используя путь к файлу или поток) и проверить его расширение.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




