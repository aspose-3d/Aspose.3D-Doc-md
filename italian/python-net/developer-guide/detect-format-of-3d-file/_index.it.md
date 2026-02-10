---
title: Rileva il formato del file 3D
type: docs
weight: 10
url: /it/python-net/detect-format-of-3d-file/
description: Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono rilevare il formato dei file 3D supportati prima di aprirlo perché l'estensione del file non garantisce che il contenuto del file sia appropriato.
---
{{% alert color="primary" %}} 

Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono rilevare il formato dei file 3D supportati prima di aprirlo perché l'estensione del file non garantisce che il contenuto del file sia appropriato.

{{% /alert %}} 
##  **Rileva il campione di programmazione del formato**
Il seguente codice di esempio illustra come rilevare un formato di file (utilizzando il percorso o lo streaming del file) e verificarne l'estensione.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
