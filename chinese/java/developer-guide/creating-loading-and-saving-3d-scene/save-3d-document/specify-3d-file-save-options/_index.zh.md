---
title: 指定 3D 文件保存选项
type: docs
weight: 10
url: /zh/java/specify-3d-file-save-options/
description: 有几个场景。保存方法重载接受一个SaveOptions实例
---
##  **3D 文件保存选项**
有几个场景。保存方法重载接受一个SaveOptions实例这应该是从SaveOptions类派生的类的实例。每种保存格式都有一个相应的类，该类保存该保存格式的保存选项，例如，FileFormat.COLLADA保存格式有ColladaSaveOptions。
###  **使用 Collada 保存选项**
下面的代码显示了如何在将 3D 文件保存为 Collada 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
###  **使用 Discreet3DS 保存选项**
下面的代码显示了如何在将 3D 文件保存为谨慎的 3DS 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
###  **使用 FBX 保存选项**
下面的代码显示了如何在将 3D 文件保存为 FBX 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
###  **使用 OBJ 保存选项**
下面的代码显示了如何在将 3D 文件保存为Obj格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
###  **使用 STL 保存选项**
下面的代码显示了如何在将 3D 文件保存为 STL 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
###  **使用 U3D 保存选项**
下面的代码显示了如何在将文档保存为 U3D 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
###  **使用 glTF 保存选项**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 



下面的代码显示了如何在将文档保存为 glTF 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
###  **glTF 保存选项中的PrettyPrint**
您还可以使用GLTFSaveOptions类的setPrettyPrint方法进行人类可理解的JSON打印。下面的代码显示了如何使用此功能。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
###  **在真实文件系统中保存 3D 场景的依赖项**
开发人员可能需要将 3D scene的所有依赖项保存在真实文件系统中。它们可以定义本地目录的路径，保存在 `MemoryFileSystem` 对象中或简单地丢弃依赖项。在all save选项类中添加了FileSystem属性。
####  **放弃保存材料文件**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
####  **在本地目录中保存依赖项**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
####  **在MemoryFileSystem实例中保存依赖项**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
###  **使用 Google Draco (.DRC) 保存选项**
下面的代码显示了如何在将 3D 模型保存为 DRC 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
###  **使用 RVM 保存选项**
下面的代码显示了如何在将 3D 模型保存为 RVM 格式之前设置保存选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
