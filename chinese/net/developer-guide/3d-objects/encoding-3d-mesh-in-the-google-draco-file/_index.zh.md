---
title: 编码 Google Draco 文件中的 3D 网格
type: docs
weight: 60
url: /zh/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API 允许开发人员导入 3D 模型，然后在 Google Draco 文件中对网格进行编码。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API 允许开发人员使用 [导入 3D 模型](/3d/zh/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene)，然后对 Google Draco 文件中的网格进行编码。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。

{{% /alert %}}
##  **检索 3D 网格并在 Google Draco 文件中编码**
[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) 类公开的 `Encode` 方法可用于对 Google Draco 文件中的3d网格进行编码。它采用 [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) 和 [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) 对象作为参数。使用 Draco 保存选项，开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。
###  **编程示例**
此代码示例检索 `Sphere` 的 `Mesh`，然后在指定压缩级别后在 Google Draco 文件中进行编码。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
            
// Create a sphere
var sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
var b = FileFormat.Draco.Encode(sphere.ToMesh(), 
    new DracoSaveOptions() { CompressionLevel = DracoCompressionLevel.Optimal });
// Save the raw bytes to file
File.WriteAllBytes(RunExamples.GetOutputFilePath("SphereMeshtoDRC_Out.drc"), b);

{{< /highlight >}}
