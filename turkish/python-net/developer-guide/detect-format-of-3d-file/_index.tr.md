---
title: 3D dosyasının biçimini algılama
type: docs
weight: 10
url: /tr/python-net/detect-format-of-3d-file/
description: Aspose.3D for Python via .NET API kullanarak, geliştiriciler dosya uzantısının dosya içeriğinin uygun olduğunu garanti etmediği için açmadan önce desteklenen 3D dosyalarının formatını algılayabilir.
---
{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API kullanarak, geliştiriciler dosya uzantısının dosya içeriğinin uygun olduğunu garanti etmediği için açmadan önce desteklenen 3D dosyalarının formatını algılayabilir.

{{% /alert %}} 
##  **Detect Format rorogramming ample ample**
Örnek kodu takip eden T, bir dosya formatının (dosya yolunu veya akışını kullanarak) nasıl algılanacağını ve uzantısını kontrol ettiğini gösterir.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
