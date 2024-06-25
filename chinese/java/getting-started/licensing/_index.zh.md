---
title: Licensing
type: docs
weight: 60
url: /zh/java/licensing/
description: 您可以轻松地从 Aspose 存储库下载/安装 Aspose.3D for Java 以进行评估。评估下载与购买的下载相同。当您添加几行代码以应用许可证时，评估版只会获得许可。
---
##  **评估 Aspose。3D**
您可以轻松地从 [Aspose 存储库](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) 下载/安装 Aspose.3D for Java 进行评估。评估下载与购买的下载相同。当您添加几行代码以应用许可证时，评估版只会获得许可。

评估版本提供了除以下功能外的所有功能:

- 用户最多只能打开/导入50个 3D 文档到场景。
- 用户最多只能将50个 3D 文档保存到场景中。
- 用户还将在渲染的图像和所有其他输出文件中看到评估水印。
- 每个节点的子节点不得超过5个。
- 每个节点可以有不超过2个附加实体。
- 每个几何图形可以有不超过2个附加顶点元素。
- 每个节点可以有不超过1个材质。

{{% alert color="primary" %}} 

如果您在没有适当许可证的情况下使用 Aspose.3D，则可能会触发**com.aspose.threed.TrialException**当使用达到未许可限制时，可以通过以下方式关闭异常:

* [购买全功能许可证](https://purchase.aspose.com/buy)。
* 申请30天临时许可证，请参阅 [如何获得临时许可证？](https://purchase.aspose.com/temporary-license) 了解更多信息。
.
* 在您的 `open`/`save` 方法之前调用 `com.aspose.threed.TrialException.setSuppressTrialException(true)`，在 `open`/`save` 调用期间不会提高 `TrialException`，但不会取消上述限制。
* 手动在 `Scene.open/save` 上使用 `try/catch` 块，此异常只是一个通知，忽略它不会影响场景加载/保存。

{{% /alert %}} 
##  **申请许可证**
许可证是一个纯文本XML文件，其中包含详细信息，例如产品名称，许可给它的开发人员数量，订阅到期日期等。文件是数字签名的，所以不要修改文件; 即使无意中在文件中添加了额外的换行符也会使它无效。在对文档执行任何操作之前，您需要设置许可证。确保在创建场景对象之前执行此操作。

可以从各个位置申请许可证:

- 显式路径
- 包含 Aspose.3D 的JAR文件的文件夹。
- JAR中调用 Aspose.3D JAR的嵌入资源。

使用 `License.setLicense` 方法许可api。通常，设置许可证的最简单方法是将许可证文件放在与 Aspose.3D 的JAR相同的文件夹中，并仅指定文件名而不指定路径。
###  **使用文件或流对象应用许可证**
在此示例中，Aspose.3D 将尝试在包含应用程序jar的文件夹中查找许可证文件。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

从流初始化许可证。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
###  **包括许可证文件作为嵌入式资源**
您可以简单地将LIC文件复制到项目的 `resources` 文件夹中。重建项目应该嵌入.lic文件到应用程序的。jar文件。之后，您可以使用下面的代码申请许可证:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
###  **验证许可证**
可以验证许可证是否已正确设置。许可证类具有isLicensed字段，如果正确设置了许可证，该字段将返回true。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
##  **申请计量许可证**
Aspose.3D 允许开发人员应用计量密钥。这是一种新的许可机制。新的许可机制将与现有的许可方法一起使用。那些希望根据 API 功能的使用情况计费的客户可以使用计量许可。更多详情，请参阅 [计量常见问题 Licensing](https://purchase.aspose.com/faqs/licensing/metered) 部分。

引入了新的类 `Metered` 以应用计量密钥。以下是演示如何设置计量公钥和私钥的示例代码。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
##  **何时申请许可证**
遵循以下简单规则:

- 每个应用程序域只需要设置一次许可证。
- 在使用任何其他 Aspose.3D 类之前，您需要设置许可证。
- 多次调用License.SetLicense不会有害，只是浪费处理器时间。

如果您正在开发类库，则可以从使用 Aspose.3D 的类的静态构造函数中调用License.SetLicense。静态构造函数将在创建类的实例之前执行，确保正确设置了 Aspose.3D 许可证。
##  **您可以更改许可证文件名**
许可证文件名不必为 'Aspose.3D.LIC'。您可以将其重命名为您喜欢的任何名称，并在调用License.SetLicense时使用该名称。
##  **异常找不到许可证文件名**
当您购买并下载许可证时，Aspose 网站会将许可证文件命名为 `Aspose.3D.LIC`。使用浏览器下载许可证文件。一些浏览器将许可证文件识别为XML并附加一个。xml扩展名，因此计算机上文件的全名变为 `Aspose.3D.lic.XML`。

例如，当将 Microsoft Windows 配置为隐藏已知文件类型的扩展名时 (不幸的是，这是大多数 Windows 安装中的默认值)，许可证文件将在 Windows 资源管理器中显示为 `Aspose.3D.LIC`。你可能会认为这是真正的文件名和调用License.SetLicense通过它 `Aspose.3D.LIC`，但没有这样的文件，因此例外。

为了解决这个问题，重命名文件以删除不可见的。xml扩展名。我们还建议您禁用 Microsoft Windows 中的 “隐藏扩展” 选项。

##  **使用来自 Aspose 的多个api**
如果您在应用程序中使用多个 Aspose api，例如 Aspose.3D 和 Aspose.Cell，这里有一些有用的提示。

- 分别为每个 Aspose API 设置许可证。即使您有一个用于所有api的许可证文件，例如 `Aspose.Total.lic`，您仍然需要为您在应用程序中使用的每个 Aspose API 单独调用 `License.setLicense`。
- 使用完全限定的许可证类名称。每个 Aspose API 在其命名空间中都有一个许可证类。例如，Aspose.3D 有 `com.aspose.3d.License` 和 Aspose。单元格有 `com.aspose.cells.License` 类。使用完全限定的类名可以避免混淆哪个许可证应用于哪个产品。
