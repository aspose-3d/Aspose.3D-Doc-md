---
title: VRML formatı ile çalışmak
type: docs
weight: 90
url: /tr/java/working-with-vrml-format/
description: Aspose.3D for Java allows working with VRML version 1.0. VRML file format has been added to the FileFormat class. Aspose.3D can auto detect VRML format, so the FileFormat is usually ignored in Open method.
---
#  **Open VRML File Format**
Aspose.3D for Java allows working with VRML version 1.0. `VRML` file format has been added to the `FileFormat` class. Aspose.3D can auto detect `VRML` format, so the `FileFormat` is usually ignored in Open method. The following code snippet shows how open VRML file format.

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
