---
title: Detectar formato de archivo 3D
type: docs
weight: 10
url: /es/python-net/detect-format-of-3d-file/
description: Con Aspose.3D for Python via .NET API, los desarrolladores pueden detectar el formato de los archivos 3D antes de abrirlo porque la extensión de archivo no garantiza que el contenido del archivo sea apropiado.
---
{{% alert color="primary" %}} 

Con Aspose.3D for Python via .NET API, los desarrolladores pueden detectar el formato de los archivos 3D antes de abrirlo porque la extensión de archivo no garantiza que el contenido del archivo sea apropiado.

{{% /alert %}} 
##  **Detectar formato de muestra de programación**
El siguiente código de ejemplo ilustra cómo detectar un formato de archivo (usando la ruta de acceso o flujo de archivo) y comprobar su extensión.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
