---
title: 在 C# 中指定 3D 文件保存选项
linktitle: 指定 3D 文件保存选项
type: docs
weight: 40
url: /zh/net/specify-3d-file-save-options/
description: 有几个场景。保存方法重载接受一个SaveOptions对象。每种保存格式都有一个相应的类，该类保存该保存格式的保存选项。
---
##  **概述**

本文介绍如何使用 C# 将 3D 文件保存为不同的格式 [将它们加载到场景对象后](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)。通过加载和保存，您可以执行不同的转换数量。

- 在 C# 中将 FBX 转换为X
- 在 C# 中将 GLTF 转换为 OBJ
- 在 C# 中将 OBJ 转换为X
- 在 C# 中将 STL 转换为 OBJ
- 在 C# 中将 RVM 转换为 3DS

##  **3D 文件保存选项**
有几个接受SaveOptions对象的 [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) 方法重载。这应该是从 `SaveOptions` 类派生的类的对象。每种保存格式都有一个对应的类，该类包含该保存格式的保存选项，例如，对于 `FileFormat.Collada` 保存格式，有 `ColladaSaveOptions`。
###  **使用 Collada 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为 Collada 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
###  **使用 Discreet3DS 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为谨慎的 3DS 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
###  **使用 FBX 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为 FBX 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` 还公开了 `EnableCompression` 属性，该属性可用于压缩 FBX 文件中的大型二进制数据。此属性的默认值为true。下面的代码片段解释了如何在保存场景时使用此属性。



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
###  **使用Obj保存选项**
下面的代码显示了如何在将 3D 文件保存为Obj格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
###  **使用 STL 保存选项**
下面的 C# 代码显示了如何在将 3D 文件保存为 STL 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
###  **使用 U3D 保存选项**
下面的 C# 代码显示了如何在将文档保存为 U3D 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
###  **使用 glTF 保存选项**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 



下面的 C# 代码显示了如何在将文档保存为 glTF 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
###  **glTF 保存选项中的PrettyPrint**
您还可以使用GLTFSaveOptions类的PrettyPrint属性进行人类可理解的JSON打印。下面的代码显示了如何使用此功能。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
###  **在真实文件系统中保存 3D 场景的依赖项**
开发人员可能需要将所有 3D 场景依赖项保存在真实文件系统中。它们可以定义本地目录的路径，保存在 `MemoryFileSystem` 对象中或简单地丢弃依赖项。`FileSystem` 属性被添加到所有保存选项类中。
####  **放弃保存材料文件**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
####  **在本地目录中保存依赖项**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
####  **在MemoryFileSystem对象中保存依赖关系**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
###  **使用 Google Draco (.drc) 保存选项**
下面的 C# 代码显示了如何在将 3D 模型保存为 DRC 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
###  **使用 RVM 保存选项**
下面的 C# 代码显示了如何在将 3D 模型保存为 RVM 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
