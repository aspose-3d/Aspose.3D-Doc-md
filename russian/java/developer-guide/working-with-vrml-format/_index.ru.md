---
title: Работа с форматом VRML
type: docs
weight: 90
url: /ru/java/working-with-vrml-format/
description: Aspose.3D for Java позволяет работать с VRML версии 1,0. Формат файла VRML добавлен в класс FileFormat. Aspose.3D может автоматически определять формат VRML, поэтому формат FileFormat обычно игнорируется в методе Open.
---
#  **Открыть формат файла VRML**
Aspose.3D for Java позволяет работать с VRML версии 1,0. Формат файла `VRML` добавлен в класс `FileFormat`. Aspose.3D может автоматически определять формат `VRML`, поэтому `FileFormat` обычно игнорируется в методе Open. Следующий фрагмент кода показывает, как открыть формат файла VRML.

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
