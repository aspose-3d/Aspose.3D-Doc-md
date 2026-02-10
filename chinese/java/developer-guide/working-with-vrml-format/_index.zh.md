---
title: 使用 VRML 格式
type: docs
weight: 90
url: /zh/java/working-with-vrml-format/
description: Aspose.3D for Java 允许使用 VRML 版本1.0。VRML 文件格式已添加到FileFormat类中。Aspose.3D 可以自动检测 VRML 格式，因此在Open方法中通常忽略FileFormat。
---
#  **打开 VRML 文件格式**
Aspose.3D for Java 允许使用 VRML 版本1.0。`VRML` 文件格式已添加到 `FileFormat` 类。Aspose.3D 可以自动检测 `VRML` 格式，因此在Open方法中通常忽略 `FileFormat`。下面的代码片段显示了如何打开 VRML 文件格式。

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
