---
title: Работа с форматом VRML
type: docs
weight: 120
url: /ru/net/working-with-vrml-format/
description: Aspose.3D for .NET позволяет работать с VRML версии 1,0. Формат файла VRML добавлен в класс FileFormat. Aspose.3D может автоматически определять формат, поэтому FileFormat обычно игнорируется в методе Open. Следующий фрагмент кода показывает, как открыть формат файла VRML.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,4 или выше.

{{% /alert %}} 
#  **Открыть формат файла VRML**
Aspose.3D for .NET позволяет работать с VRML версии 1,0. Формат файла `VRML` добавлен в класс `FileFormat`. Aspose.3D может автоматически определять формат, поэтому `FileFormat` обычно игнорируется в методе `Open`. Следующий фрагмент кода показывает, как открыть формат файла VRML.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Open Virtual Reality Modeling Language (VRML) file format
scene.Open("test.wrl");
// Work with VRML file format...


{{< /highlight >}}
