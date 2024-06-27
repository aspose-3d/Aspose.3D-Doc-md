---
title: 保存 3D 场景时导出纹理文件
type: docs
weight: 10
url: /zh/net/export-texture-files-while-saving-3d-scene
description: 使用 Aspose.3D for .NET，开发人员可以将纹理文件导出到文件系统，同时保存 3D 场景。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，将场景导出到文件时，通常需要将纹理 (无论是嵌入的还是外部的) 导出到同一目录。Aspose.3D for .NET 有助于此过程，确保所有纹理与导出的场景一起得到正确管理和存储。本指南演示了如何实现这一点。

{{% /alert %}}

要导出场景并确保所有关联的纹理都保存到同一目录，请按照下列步骤操作:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Aspose.3D 中的所有 `SaveOptions` 对象都包含 `ExportTextures` 属性，这简化了导出期间管理纹理的过程。此属性可确保所有纹理 (无论是外部的还是嵌入的) 都保存到指定的输出目录。此功能与支持纹理导出的各种文件格式兼容，例如 FBX 、 3DS 、 OBJ 、 USD 、 GLTF 和 DAE。



说明

1. 加载场景: 从输入文件加载场景。
1. 配置保存选项: 将 `ExportTextures` 设置为 `true`。
1. 导出场景: 使用更新的纹理路径将场景保存到输出目录。


通过利用 `SaveOptions` 中的 `ExportTextures` 属性，您可以无缝地导出 3D 场景及其纹理，确保所有必要的资源都组织在一个目录中。此功能增强了 3D 文件跨各种平台和应用程序的可移植性和易用性。

##  **资源**

1. [在线教程](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
