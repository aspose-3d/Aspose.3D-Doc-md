---
title: Licensing
type: docs
weight: 60
url: /zh/net/licensing/
description: 有关在 C# 中处理 3D 文件格式的 Licensing 要求和评估版本限制的概述。
---
有关在 C# 中处理 3D 文件格式的 Licensing 要求和评估版本限制的概述。

##  **评估版本限制**
Aspose.3D for .NET 的免费评估版可从 Aspose 网站的 “下载” 部分下载: [下载 Aspose.3D API](https://www.nuget.org/packages/Aspose.3D)。
###  **限制**
评估版本提供了除以下功能外的所有功能:

- 用户最多只能打开/导入50个 3D 文档到场景。
- 每个节点的子节点不得超过5个。
- 每个节点可以有不超过2个附加实体。
- 每个几何图形可以有不超过2个附加顶点元素。
- 每个节点可以有不超过1个材质。
- 用户最多只能将50个 3D 文档保存到场景中。
- 用户还将在渲染的图像和所有其他输出文件中看到评估水印。

{{% alert color="primary" %}} 
如果您在没有适当许可证的情况下使用 Aspose.3D，则当使用达到未许可限制时可能会触发 `Aspose.ThreeD.TrialException`，您可以通过以下方式关闭异常:

* [购买全功能许可证](https://purchase.aspose.com/buy)。
* 申请30天临时许可证，请参阅 [如何获得临时许可证？](https://purchase.aspose.com/temporary-license) 了解更多信息。
.
* 如果将 `Aspose.ThreeD.TrialException.SuppressTrialException` 设置为 `true`，则在现场调用 `Open/Save` 时不会筹集到 `TrialException`，但不会取消上述限制。
* 手动在 `Scene.Open/Save` 上使用 `try/catch` 块，此异常只是一个通知，忽略它不会影响场景加载/保存。

{{% /alert %}} 

##  **使用文件或流对象应用许可证**
可以从 [文件](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) 或 [流对象](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject) 加载许可证。Aspose.3D for .NET 将尝试在以下位置查找许可证:

1. 显式路径。
1. 包含 Aspose.3D.dll的文件夹。
1. 包含调用 Aspose.3D.dll的程序集的文件夹。
1. 包含条目程序集 (your .exe) 的文件夹。
1. 程序集中调用 Aspose.3D.dll的嵌入资源。

设置许可证的最简单方法是将许可证文件与 Aspose.3D.dll文件放在同一文件夹中，并指定文件名，但不指定路径，如下例所示。

{{% alert color="primary" %}} 

如果您使用的是任何其他 Aspose for .NET API 以及 Aspose.3D for .NET，请指定许可证的命名空间，如 `Aspose.ThreeD.License`。

{{% /alert %}} 
###  **从文件加载许可证**
应用许可证的最简单方法是将许可证文件与 Aspose.3D.dll文件放在同一文件夹中，并仅指定文件名而不指定路径。

{{% alert color="primary" %}} 

当您调用 `SetLicense` 方法时，您传递的许可证名称应该是许可证文件的名称。例如，如果将许可证文件名更改为 “Aspose.3D.lic.xml”，请将该文件名传递给 `threeD.SetLicense(…)` 方法。

{{% /alert %}} 

**示例:**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
###  ` `**从流对象加载许可证**
下面的示例演示如何从流加载许可证。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
FileStream myStream = new FileStream("Aspose._3D.lic", FileMode.Open);
license.SetLicense(myStream);

{{< /highlight >}}
##  **使用嵌入式资源申请许可证**
应用许可证的一种方法是将其设置为 [使用文件或流对象]()。将许可证与您的应用程序打包并确保它不会丢失的另一种巧妙方法是将其作为嵌入式资源包含到调用组件的DLL的程序集中 (包含在 Aspose.3D 中)。

要将许可证文件包含为嵌入式资源:

1. 在Visual Studio .NET 中，通过选择**文件**,那么**添加现有项目**最后**添加**.
1. 在解决方案资源管理器中选择文件。
1. 设置**构建行动**到**嵌入式资源**在属性窗口中。
1. 要访问嵌入在程序集中的许可证 (作为嵌入式资源)，只需将许可证文件作为嵌入式资源添加到项目中，并将许可证文件的名称传递给SetLicense方法。许可证类会自动在嵌入的资源中查找许可证文件。无需调用 Microsoft .NET 框架中的System.Reflection.Assembly类的GetExecutingAssembly和GetManifestResourceStream方法。

下面的代码片段用于设置许可证。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Instantiate the License class
Aspose.ThreeD.License license = new Aspose.ThreeD.License();

// Pass only the name of the license file embedded in the assembly
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
##  **申请计量许可证**
Aspose.3D for .NET API 允许开发人员应用计量许可证。这是一种新的许可机制。新的许可机制将与现有的许可方法一起使用。那些希望根据 API 功能的使用情况计费的客户可以使用计量许可。详情请参阅 [计量常见问题 Licensing](https://purchase.aspose.com/faqs/licensing/metered) 部分。

添加了新的类 [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) 以应用计量密钥。此代码示例演示如何设置计量公钥和私钥:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a Metered license class object
Aspose.ThreeD.Metered metered = new Aspose.ThreeD.Metered();
// Set public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
