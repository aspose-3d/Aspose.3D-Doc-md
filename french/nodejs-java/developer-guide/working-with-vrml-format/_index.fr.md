---
title: Travailler avec VRML Format
type: docs
weight: 90
url: /fr/nodejs-java/working-with-vrml-format/
description: Aspose.3D for Node.js via Java permet de travailler avec VRML version 1.0. Le format de fichier VRML a été ajouté à la classe FileFormat. Aspose.3D peut détecter automatiquement le format VRML, donc FileFormat est généralement ignoré dans la méthode Open.
---
#  **Ouvrir le format de fichier VRML**
Aspose.3D for Node.js via Java permet de travailler avec VRML version 1.0. Le format de fichier `VRML` a été ajouté à la classe `FileFormat`. Aspose.3D peut détecter automatiquement le format `VRML`, de sorte que le `FileFormat` est généralement ignoré dans la méthode Open. L'extrait de code suivant montre comment ouvrir le format de fichier VRML.

{{< highlight "java" >}}

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
