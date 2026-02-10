---
title: Détecter le format du fichier 3D
type: docs
weight: 10
url: /fr/python-net/detect-format-of-3d-file/
description: En utilisant Aspose.3D for Python via .NET API, les développeurs peuvent détecter le format des fichiers 3D pris en charge avant de l'ouvrir car l'extension de fichier ne garantit pas que le contenu du fichier est approprié.
---
{{% alert color="primary" %}} 

En utilisant Aspose.3D for Python via .NET API, les développeurs peuvent détecter le format des fichiers 3D pris en charge avant de l'ouvrir car l'extension de fichier ne garantit pas que le contenu du fichier est approprié.

{{% /alert %}} 
##  **Détecter l'échantillon de programmation de format**
L'exemple de code suivant illustre comment détecter un format de fichier (à l'aide du chemin de fichier ou du flux) et vérifier son extension.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
