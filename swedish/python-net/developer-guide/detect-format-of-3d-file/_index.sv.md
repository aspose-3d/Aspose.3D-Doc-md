---
title: Upptäck format för 3D-filen
type: docs
weight: 10
url: /sv/python-net/detect-format-of-3d-file/
description: Använder Aspose.3D for Python via .NET API utvecklare kan upptäcka formatet för stödda 3D filer innan den öppnas eftersom filändelsen inte garanterar att filinnehållet är lämpligt Te.
---
{{% alert color="primary" %}} 

Använder Aspose.3D for Python via .NET API utvecklare kan upptäcka formatet för stödda 3D filer innan den öppnas eftersom filändelsen inte garanterar att filinnehållet är lämpligt Te.

{{% /alert %}} 
##  **Detektera formatprogrammeringsprover**
Följande kod illustrerar hur man upptäcker ett filformat (med hjälp av filvägen eller strömmen) och kontrollera dess tillägg.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
