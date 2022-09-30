---
title: 在C#中指定3D文件保存选项
linktitle: 指定3D文件保存选项
type: docs
weight: 40
url: /zh/net/specify-3d-file-save-options/
description: 有几个场景。保存方法重载接受一个SaveOptions对象。每种保存格式都有一个相应的类，该类保存该保存格式的保存选项。
---
## **概述**

本文介绍了如何将3D文件保存为不同的格式[将它们加载到场景对象后](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)使用C#。通过加载和保存，您可以执行许多不同的转换，例如

- 将C#中的FBX转换为X
- 在C#中将GLTF转换为OBJ
- 将C#中的OBJ转换为X
- 在C#中将STL转换为OBJ
- 在C#中将RVM转换为3DS

## **3D文件保存选项**
有几个[`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene)方法重载接受一个SaveOptions对象。这应该是从`SaveOptions`类派生的类的对象。每个保存格式都有一个相应的类，该类保存该保存格式的保存选项，例如，存在`FileFormat.Collada`保存格式的`ColladaSaveOptions`。
### **使用Collada保存选项**
下面的C#代码显示了如何在将3D文件保存为Collada格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **使用Discreet3DS保存选项**
下面的C#代码显示了如何在将3D文件保存为谨慎的3DS格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **使用FBX保存选项**
下面的C#代码显示了如何在将3D文件保存为FBX格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions`还公开了可用于压缩FBX文件中的大二进制数据的`EnableCompression`属性。此属性的默认值为true。下面的代码片段解释了如何在保存场景时使用此属性。



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **使用Obj保存选项**
下面的代码显示了如何在将3D文件保存为Obj格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **使用STL保存选项**
下面的C#代码显示了如何在将3D文件保存为STL格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **使用U3D保存选项**
下面的C#代码显示了如何在将文档保存为U3D格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **使用glTF保存选项**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 



下面的C#代码显示了如何在将文档保存为glTF格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **PrettyPrint在glTF保存选项**
您还可以使用GLTFSaveOptions类的PrettyPrint属性进行人类可理解的JSON打印。下面的代码显示了如何使用此功能。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **在真实文件系统中保存3D场景的依赖关系**
开发人员可能需要将所有3D场景依赖项保存在真实文件系统中。它们可以定义本地目录的路径，保存在`MemoryFileSystem`对象中或简单地丢弃依赖项。`FileSystem`属性被添加到all save选项类中。
#### **放弃保存材料文件**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **在本地目录中保存依赖项**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **在MemoryFileSystem对象中保存依赖关系**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **使用Google Draco (.drc) 保存选项**
下面的C#代码显示了如何在将3D模型保存为DRC格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **使用RVM保存选项**
下面的C#代码显示了如何在将3D模型保存为RVM格式之前设置保存选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
