---
title: 编码 Google Draco 文件中的 3D 网格
type: docs
weight: 30
url: /zh/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API 支持在 Google Draco 文件中导入 3D 模型、检索网格，然后对网格进行编码。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持在 Google Draco 文件中导入 3D 模型、检索网格，然后对网格进行编码。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。

{{% /alert %}} 
##  **在 Google Draco 文件中检索 3D 网格和编码**
`DracoFormat` 类公开的encode方法可用于对 Google Draco 文件中的 3D 网格进行编码。它采用 `Mesh` 和 `DracoSaveOptions` 对象作为参数。使用 Draco 保存选项，开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。
###  **编程示例**
此代码示例检索球体的网格，然后在指定压缩级别后在 Google Draco 文件中进行编码。

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
