---
title: 使用 VRML 格式
type: docs
weight: 120
url: /zh/python-net/working-with-vrml-format/
description: Aspose.3D for Python via .NET 允许使用 VRML 版本1.0。VRML 文件格式已添加到FileFormat类中。Aspose.3D 可以自动检测格式，因此FileFormat通常在Open方法中被忽略。下面的代码片段显示了如何打开 VRML 文件格式。
---
{{% alert color="primary" %}} 

19.4或更高版本支持此功能。

{{% /alert %}} 
#  **打开 VRML 文件格式**
Aspose.3D for Python via .NET 允许使用 VRML 版本1.0。`VRML` 文件格式已添加到 `FileFormat` 类。Aspose.3D 可以自动检测格式，因此 `FileFormat` 通常在 `open` 方法中被忽略。下面的代码片段显示了如何打开 VRML 文件格式。

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
