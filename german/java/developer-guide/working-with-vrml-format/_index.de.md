---
title: Arbeiten mit dem VRML-Format
type: docs
weight: 90
url: /de/java/working-with-vrml-format/
description: Aspose.3D for Java ermöglicht die Arbeit mit VRML Version 1.0. Das Dateiformat VRML wurde der FileFormat-Klasse hinzugefügt. Aspose.3D kann das VRML-Format automatisch erkennen, sodass das File Format in der Open-Methode normaler weise ignoriert wird.
---
#  **Öffnen Sie VRML-Dateiformat**
Aspose.3D for Java ermöglicht die Arbeit mit VRML Version 1.0. Das Dateiformat `VRML` wurde der Klasse `FileFormat` hinzugefügt. Aspose.3D kann das `VRML`-Format automatisch erkennen, sodass die `FileFormat` in der Open-Methode normaler weise ignoriert werden. Das folgende Code-Snippet zeigt, wie öffnen VRML Dateiformat.

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
