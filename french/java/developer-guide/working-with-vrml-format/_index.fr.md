---
title: Travailler avec VRML Format
type: docs
weight: 90
url: /fr/java/working-with-vrml-format/
description: Aspose.3D for Java permet de travailler avec VRML version 1.0. Le format de fichier VRML a été ajouté à la classe FileFormat. Aspose.3D peut détecter automatiquement le format VRML, de sorte que le FileFormat est généralement ignoré dans la méthode Open.
---
#  **Ouvrir le format de fichier VRML**
Aspose.3D for Java permet de travailler avec VRML version 1.0. Le format de fichier `VRML` a été ajouté à la classe `FileFormat`. Aspose.3D peut détecter automatiquement le format `VRML`, donc `FileFormat` est généralement ignoré dans la méthode Open. L'extrait de code suivant montre comment ouvrir le format de fichier VRML.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// open Virtual Reality Modeling Language (VRML) file format
scene.open( MyDir + "test.wrl");
// work with VRML file format...

{{< /highlight >}}
