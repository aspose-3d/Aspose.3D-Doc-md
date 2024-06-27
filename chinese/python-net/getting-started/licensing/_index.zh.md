---
title: Licensing
description: Aspose.3D for Python via .NET 提供不同的购买计划，或使用 Licensing 和订阅政策提供免费试用和30天的评估临时许可证
type: docs
weight: 80
url: /zh/python-net/licensing/
---
有时，为了更好地研究系统，您希望尽可能快地深入代码。为了简化操作，Aspose.3D 提供了不同的购买计划，或者提供了免费试用和30天的评估临时许可证。

{{% alert color="primary" %}}

请注意，有许多一般政策和实践指导您如何评估、正确许可和购买我们的产品。您可以在 [“购买政策和常见问题”](https://purchase.aspose.com/policies) 部分中找到它们。

{{% /alert %}}

##  **评估 Aspose。3D**
您可以轻松下载 Aspose.3D 进行评估。评估包与购买的包相同。在您添加几行代码以应用许可证后，评估版只会获得许可。

##  **评估版本限制**
评估版本提供了除以下功能外的所有功能:

- 用户最多只能打开/导入50个 3D 文档到场景。
- 每个节点的子节点不得超过5个。
- 每个节点可以有不超过2个附加实体。
- 每个几何图形可以有不超过2个附加顶点元素。
- 每个节点可以有不超过1个材质。
- 用户最多只能将50个 3D 文档保存到场景中。
- 用户还将在渲染的图像和所有其他输出文件中看到评估水印。

{{% alert color="primary" %}} 
如果您在没有适当许可证的情况下使用 Aspose.3D，则当使用达到未许可限制时可能会触发 `aspose.threed.TrialException`，您可以通过以下方式关闭异常:

* [购买全功能许可证](https://purchase.aspose.com/buy)。
* 申请30天临时许可证，请参阅 [如何获得临时许可证？](https://purchase.aspose.com/temporary-license) 了解更多信息。
* 手动在 `Scene.open/save` 上使用 `try/except` 块，此异常只是一个通知，忽略它不会影响场景加载/保存。

{{% /alert %}} 


##  **关于许可证**
您可以从 [下载页面](https://pypi.org/project/aspose.3d/) 轻松下载 Aspose.3D for Python via .NET 的评估版。评估版本提供绝对**同样的能力**作为 Aspose.3D 的许可版本。此外，在您购买许可证并添加几行代码以应用许可证后，评估版只会获得许可。

许可证是一个纯文本XML文件，其中包含详细信息，例如产品名称，许可给它的开发人员数量，订阅到期日期等。文件是数字签名的，所以不要修改文件。即使在文件内容中无意添加额外的换行符也会使其无效。

为了避免与评估版本相关的限制，您需要在使用前设置许可证**Aspose.3D**。每个应用程序或过程只需要设置一次许可证。

## 购买许可证

购买后，您需要应用许可证文件或流。本节介绍如何做到这一点的选项，并对一些常见问题进行评论。

{{% alert color="primary" %}}

您需要设置许可证:
* 每个应用程序域仅一次
* 在使用任何其他 Aspose.3D 类之前

{{% /alert %}}

{{% alert color="primary" %}}

您可以在 [“定价信息”](https://purchase.aspose.com/pricing/3d/family) 页面上找到定价信息。

{{% /alert %}}

###  **在 Aspose.3D for Python via .NET 中设置许可证**

可以从各个位置申请许可证:

* 显式路径
* 包含调用 Aspose.3D for Python via .NET 的python脚本的文件夹
* 溪流
* 作为计量许可证-一种新的许可机制

{{% alert color="primary" %}}

使用 `set_license` 方法许可组件。

多次调用 `set_license` 是无害的，它只是浪费处理器时间。

{{% /alert %}}

在下面的部分中，我们将描述用于设置许可证的两种常用方法。

####  **使用文件申请许可证**
设置许可证的最简单方法要求您将许可证文件放在包含为 Python 调用 Aspose.3D 的python脚本的同一文件夹中，并仅指定文件名而不指定其路径。

此代码段用于设置许可证文件:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

调用 `set_license` 方法时，许可证名称应与许可证文件的名称相同。例如，可以将许可证文件名更改为 “Aspose.3D.lic.xml”。然后，在您的代码中，您必须将新的许可证名称 (Aspose.3D.lic.xml) 传递给SetLicense方法。

####  **从流中申请许可证**
您可以从流加载许可证。

此代码段用于从流中应用许可证:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### 申请计量许可证

Aspose.3D 允许开发人员应用计量密钥。这是一种新的许可机制。

新的许可机制将与现有的许可方法一起使用。那些希望根据 API 功能的使用情况计费的客户可以使用计量的 Licensing。

完成获取此类许可证的所有必要步骤后，您将收到密钥，而不是许可证文件。可以使用专门为此目的引入的 `Metered` 类来应用此计量密钥。

下面的代码示例演示如何设置计量公钥和私钥:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

请注意，您必须具有稳定的Internet连接才能正确使用计量许可证，因为计量机制需要与我们的服务不断交互才能进行正确的计算。有关详细信息，请参阅 [“计量的 Licensing 常见问题”](https://purchase.aspose.com/faqs/licensing/metered) 部分。

{{% /alert %}}



