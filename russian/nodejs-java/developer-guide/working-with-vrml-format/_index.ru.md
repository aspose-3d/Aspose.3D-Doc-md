---
title: Работа с форматом VRML
type: docs
weight: 90
url: /ru/nodejs-java/working-with-vrml-format/
description: Aspose.3D for Node.js via Java позволяет работать с VRML версии 1,0. Формат файла VRML добавлен в класс FileFormat. Aspose.3D может автоматически определять формат VRML, поэтому формат FileFormat обычно игнорируется в методе Open.
---
#  **Открыть формат файла VRML**
Aspose.3D for Node.js via Java позволяет работать с VRML версии 1,0. Формат файла `VRML` добавлен в класс `FileFormat`. Aspose.3D может автоматически определять формат `VRML`, поэтому `FileFormat` обычно игнорируется в методе Open. Следующий фрагмент кода показывает, как открыть формат файла VRML.

{{< highlight "java" >}}

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
