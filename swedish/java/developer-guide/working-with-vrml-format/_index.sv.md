---
title: Arbetar med VRML Format
type: docs
weight: 90
url: /sv/java/working-with-vrml-format/
description: Aspose.3D for Java tillåter arbete med VRML version 1.0. VRML filformat har lagts till i klassen FileFormat. Aspose.3D kan automatiskt detektera VRML-formatet, så filformatet ignoreras vanligtvis i Öppna metoden.
---
#  **Open VRML File Format**
Aspose.3D for Java tillåter arbete med VRML version 1.0. `VRML` filformat har lagts till i `FileFormat` klassen. Aspose.3D kan automatiskt detektera `VRML`-formatet, så `FileFormat` ignoreras vanligtvis i Öppningsmetoden. Följande kodsnutt visar hur öppet VRML filformat.

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
