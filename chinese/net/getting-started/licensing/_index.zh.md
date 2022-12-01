---
title: 许可
type: docs
weight: 60
url: /zh/net/licensing/
description: C#中处理3D文件格式的许可要求和评估版本限制概述。
---
C#中处理3D文件格式的许可要求和评估版本限制概述。

## **评估版本限制**
Aspose.3D for .NET的免费评估版本可以从Aspose网站的下载部分下载:[下载Aspose.3D API](https://www.nuget.org/packages/Aspose.3D)。
### **限制**
评估版本提供了除以下功能外的所有功能:

- 用户最多只能打开/导入50个3D文档到一个场景。
- 每个节点的子节点不得超过5个。
- 每个节点可以有不超过2个附加实体。
- 每个几何图形可以有不超过2个附加顶点元素。
- 每个节点可以有不超过1个材质。
- 用户最多只能将50个3D文档保存到一个场景中。
- 用户还将在渲染的图像和所有其他输出文件中看到评估水印。

{{% alert color="primary" %}} 
如果您使用的Aspose.3D没有适当的许可证，当使用达到未许可的限制时，可能会触发`Aspose.ThreeD.TrialException`，您可以通过以下方式关闭异常:

* [购买全功能许可证](https://purchase.aspose.com/buy)。
* 请求30天的临时许可证，请参阅 [如何获得临时许可证？](https://purchase.aspose.com/临时许可证) 以获取更多信息。
。
* 将 “Aspose.ThreeD.TrialException.Supprestrialexception” 设置为 “true”，在现场的 “打开/保存” 调用期间不会引发 “TrialException”，但不会取消上述限制。
* 在 “scene.Open/save” 上手动使用 “try/catch” 块，此异常只是通知，忽略它不会影响场景加载/保存。

{{% /alert %}} 

## **使用文件或流对象应用许可证**
许可证可以从[文件](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)或者[流对象](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject).Aspose.3D for .NET将尝试在以下位置找到许可证:

1. 显式路径。
1. 包含Aspose.3D.dll的文件夹。
1. 包含调用Aspose.3D.dll的程序集的文件夹。
1. 包含条目程序集 (your .exe) 的文件夹。
1. 调用Aspose.3D.dll的程序集中的嵌入式资源。

设置许可证最简单的方法是将许可证文件与Aspose.3D.dll文件放在同一文件夹中，并指定文件名，不带路径，如下例所示。

{{% alert color="primary" %}} 

如果您使用的是任何其他Aspose for .NET API以及Aspose.3D for .NET，请像`Aspose.ThreeD.License`一样指定许可证的名称空间。

{{% /alert %}} 
### **从文件加载许可证**
应用许可证的最简单方法是将许可证文件放在与Aspose.3D.dll文件相同的文件夹中，并仅指定文件名而没有路径。

{{% alert color="primary" %}} 

当您调用`SetLicense`方法时，您传递的许可证名称应该是许可证文件的名称。例如，如果将许可证文件名更改为 “Aspose.3D.lic.xml”，则将该文件名传递给`threeD.SetLicense(…)`方法。

{{% /alert %}} 

**示例:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**从流对象加载许可证**
下面的示例演示如何从流加载许可证。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **使用嵌入式资源申请许可证**
申请许可证的一种方法是设置它[使用文件或流对象]()。将许可证与应用程序打包并确保它不会丢失的另一种巧妙方法是将其作为嵌入式资源包含到调用组件DLL (包含在Aspose.3D中) 的程序集之一中。

要将许可证文件包含为嵌入式资源:

1. 在Visual Studio .NET中，通过选择将许可证 (.lic) 文件包含到项目中**文件**,那么**添加现有项目**最后**添加**。
1. 在解决方案资源管理器中选择文件。
1. 设置**构建行动**到**嵌入式资源**在属性窗口中。
1. 要访问嵌入在程序集中的许可证 (作为嵌入式资源)，只需将许可证文件作为嵌入式资源添加到项目中，并将许可证文件的名称传递给SetLicense方法。许可证类自动在嵌入式资源中找到许可证文件。无需在Microsoft .NET框架中调用System.Reflection.Assembly类的GetExecutingAssembly和GetManifestResourceStream方法。

下面的代码片段用于设置许可证。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **申请计量许可证**
Aspose.3D for .NET API允许开发人员应用计量许可证。这是一种新的许可机制。新的许可机制将与现有的许可方法一起使用。那些希望根据API功能的使用情况进行计费的客户可以使用计量许可。有关更多详细信息，请参阅[计量许可常见问题](https://purchase.aspose.com/faqs/licensing/metered)节。

添加了一个新的类[`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered)来应用计量密钥。此代码示例演示如何设置计量公钥和私钥:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
