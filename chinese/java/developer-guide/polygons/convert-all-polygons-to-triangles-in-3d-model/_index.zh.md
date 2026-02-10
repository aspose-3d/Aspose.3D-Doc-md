---
title: 将 3D 模型中的所有多边形转换为三角形
type: docs
weight: 10
url: /zh/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API 支持在任何受支持的 3D 文档中将所有多边形转换为三角形。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持在任何受支持的 3D 文档中将所有多边形转换为三角形。

{{% /alert %}} 
##  **将所有多边形转换为三角形**
我们在 `PolygonModifier` 类中添加了另一个triangulate方法的重载，它将 `Scene` 类对象作为参数，如下代码示例所示:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene(MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.triangulate(scene);
// Save 3D scene
scene.save(MyDir + "triangulated_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
