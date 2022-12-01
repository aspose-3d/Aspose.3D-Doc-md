---
title: 指定3D文件保存选项
type: docs
weight: 10
url: /zh/java/specify-3d-file-save-options/
description: 有几个场景。保存方法重载接受一个SaveOptions实例
---
## **3D文件保存选项**
有几个场景。保存方法重载接受一个SaveOptions实例这应该是从SaveOptions类派生的类的实例。每种保存格式都有一个相应的类，该类保存该保存格式的保存选项，例如，FileFormat.COLLADA保存格式有ColladaSaveOptions。
### **使用Collada保存选项**
下面的代码显示了如何在保存Collada格式的3D文件之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **使用Discreet3DS保存选项**
下面的代码显示了如何在将3D文件保存为谨慎的3DS格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **使用FBX保存选项**
下面的代码显示了如何在将3D文件保存为FBX格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **使用OBJ保存选项**
下面的代码显示了如何在将3D文件保存为Obj格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **使用STL保存选项**
下面的代码显示了如何在将3D文件保存为STL格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **使用U3D保存选项**
下面的代码显示了如何在将文档保存为U3D格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **使用glTF保存选项**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 



下面的代码显示了如何在将文档保存为glTF格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint在glTF保存选项**
您还可以使用GLTFSaveOptions类的setPrettyPrint方法进行人类可理解的JSON打印。下面的代码显示了如何使用此功能。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **在真实文件系统中保存3D场景的依赖关系**
开发人员可能需要将3D场景的所有依赖关系保存在真实的文件系统中。它们可以定义本地目录的路径，保存在`MemoryFileSystem`对象中或简单地丢弃依赖项。文件系统属性被添加到所有保存选项类中。
#### **放弃保存材料文件**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **在本地目录中保存依赖项**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **在MemoryFileSystem实例中保存依赖项**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **使用Google Draco (.DRC) 保存选项**
下面的代码显示了如何在将3D模型保存为DRC格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **使用RVM保存选项**
下面的代码显示了如何在将3D模型保存为RVM格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
