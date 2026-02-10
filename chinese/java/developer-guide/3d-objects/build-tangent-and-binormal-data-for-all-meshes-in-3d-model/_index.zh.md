---
title: 为 3D 模型中的所有网格构建切线和二项式数据
type: docs
weight: 10
url: /zh/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: 使用 Aspose.3D for Java API，开发人员可以为任何受支持的 3D 文档中的所有网格构建切线和副法线数据。
---
{{% alert color="primary" %}} 

使用 Aspose.3D for Java API，开发人员可以为任何受支持的 3D 文档中的所有网格构建切线和副法线数据。

{{% /alert %}} 
##  **为网格构建切线和双正数据**
我们在 `PolygonModifier` 类中添加了两个 `buildTangentBinormal` 方法。一个方法将 `Scene` 类对象作为参数，另一个方法将 `Mesh` 类对象作为参数，如下代码示例所示:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene( MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.buildTangentBinormal(scene);
// Save 3D scene
scene.save(MyDir + "BuildTangentAndBinormalData_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
