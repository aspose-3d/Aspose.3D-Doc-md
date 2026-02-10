---
title: Travailler avec VRML Format
type: docs
weight: 120
url: /fr/python-net/working-with-vrml-format/
description: Aspose.3D for Python via .NET permet de travailler avec VRML version 1.0. Le format de fichier VRML a été ajouté à la classe FileFormat. Aspose.3D peut détecter automatiquement le format, donc le FileFormat est généralement ignoré dans la méthode Open. L'extrait de code suivant montre comment ouvrir le format de fichier VRML.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.4 ou supérieure.

{{% /alert %}} 
#  **Ouvrir le format de fichier VRML**
Aspose.3D for Python via .NET permet de travailler avec VRML version 1.0. Le format de fichier `VRML` a été ajouté à la classe `FileFormat`. Aspose.3D peut détecter automatiquement le format, de sorte que `FileFormat` est généralement ignoré dans la méthode `open`. L'extrait de code suivant montre comment ouvrir le format de fichier VRML.

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
