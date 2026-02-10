---
title: Определение формата файла 3D
type: docs
weight: 10
url: /ru/python-net/detect-format-of-3d-file/
description: Используя Aspose.3D for Python via .NET API, разработчики могут определить формат поддерживаемых 3D файлов перед их открытием, поскольку расширение файла не гарантирует, что содержимое файла подходит.
---
{{% alert color="primary" %}} 

Используя Aspose.3D for Python via .NET API, разработчики могут определить формат поддерживаемых 3D файлов перед их открытием, поскольку расширение файла не гарантирует, что содержимое файла подходит.

{{% /alert %}} 
##  **Обнаружить образец программирования формата**
Следующий образец кода иллюстрирует, как обнаружить формат файла (используя путь к файлу или поток) и проверить его расширение.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
