---
title: Travailler avec VRML Format
type: docs
weight: 120
url: /fr/net/working-with-vrml-format/
description: Aspose.3D for .NET permet de travailler avec VRML version 1.0. Le format de fichier VRML a été ajouté à la classe FileFormat. Aspose.3D peut détecter automatiquement le format, de sorte que FileFormat est généralement ignoré dans la méthode Open. L'extrait de code suivant montre comment ouvrir le format de fichier VRML.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.4 ou supérieure.

{{% /alert %}} 
#  **Ouvrir le format de fichier VRML**
Aspose.3D for .NET permet de travailler avec VRML version 1.0. Le format de fichier `VRML` a été ajouté à la classe `FileFormat`. Aspose.3D peut détecter automatiquement le format, de sorte que `FileFormat` est généralement ignoré dans la méthode `Open`. L'extrait de code suivant montre comment ouvrir le format de fichier VRML.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Open Virtual Reality Modeling Language (VRML) file format
scene.Open("test.wrl");
// Work with VRML file format...


{{< /highlight >}}
