---
title: 使用 C# 以不同的 3D 格式保存 3D 文档
linktitle: 保存 3D 文档
type: docs
weight: 20
url: /zh/net/save-a-3d-document/
description: Aspose.3D API 的Scene类表示 3D 文档，开发人员可以将其对象保存为任何支持的文件格式。
---
##  **概述**
本文介绍如何使用 C# 3D 文档处理库以各种格式保存 3D 文档，包括

- 使用 C# 以 FBX 格式保存 3D 文档-AutoDesk
- 使用 C# - Collada 以 DAE 格式保存 3D 文档
- 使用 C# - Discreet 3D Studio以 3DS 格式保存 3D 文档
- 使用 C# - Google Draco 以 DRC 格式保存 3D 文档

{{% alert color="primary" %}} 

Aspose.3D API 的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类表示 3D 文档，开发人员可以将其对象保存为任何支持的文件格式。要保存 3D 场景，只需使用 [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) 方法，它接受具有完整路径的文件名或文件流对象。Aspose.3D API 提供另一个 `FileFormat` 参数来指定输出文件格式。

{{% /alert %}} 

##  **以支持的 3D 格式保存 3D 场景**

下面的 C# 代码示例显示了如何将 3D 场景或文档以各种支持的 3D 格式保存到流中。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
