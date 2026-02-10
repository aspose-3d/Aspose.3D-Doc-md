---
title: Erkennen Sie das Format der 3D-Datei
type: docs
weight: 10
url: /de/python-net/detect-format-of-3d-file/
description: Mit Aspose.3D for Python via .NET API können Entwickler das Format der unterstützten 3D-Dateien vor dem Öffnen erkennen, da die Datei erweiterung nicht garantiert, dass der Datei inhalt angemessen ist.
---
{{% alert color="primary" %}} 

Mit Aspose.3D for Python via .NET API können Entwickler das Format der unterstützten 3D-Dateien vor dem Öffnen erkennen, da die Datei erweiterung nicht garantiert, dass der Datei inhalt angemessen ist.

{{% /alert %}} 
##  **Muster für die Format programmierung erkennen**
Der folgende Beispielcode ver anschaulicht, wie Sie ein Dateiformat (mithilfe des Datei pfads oder-stroms) erkennen und dessen Erweiterung überprüfen.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
