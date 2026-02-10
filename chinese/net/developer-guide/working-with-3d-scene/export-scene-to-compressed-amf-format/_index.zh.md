---
title: 将场景导出为压缩的 AMF 格式
type: docs
weight: 30
url: /zh/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET 提供AmfSaveOptions类，允许您根据需要设置压缩的bool值。默认情况下，该值设置为true。
---
##  **将场景导出为压缩的 AMF 格式**
Aspose.3D for .NET 提供 `AmfSaveOptions` 类，允许您根据需要设置压缩的bool值。默认情况下，该值设置为true。以下代码段显示了生成压缩的 AMF 格式文件的完整功能:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load a scene
Scene scene = new Scene();
var box = new Box();
var tr = scene.RootNode.CreateChildNode(box).Transform;
tr.Scale = new Vector3(12, 12, 12);
tr.Translation = new Vector3(10, 0, 0);
tr = scene.RootNode.CreateChildNode(box).Transform;
// Scale transform
tr.Scale = new Vector3(5, 5, 5);
// Set Euler Angles
tr.EulerAngles = new Vector3(50, 10, 0);
scene.RootNode.CreateChildNode();
scene.RootNode.CreateChildNode().CreateChildNode(box);
scene.RootNode.CreateChildNode().CreateChildNode(box);
// Save compressed AMF file
scene.Save("Aspose.amf", new AmfSaveOptions() { EnableCompression = false });

{{< /highlight >}}
