---
title: Declaration
type: docs
weight: 30
url: /zh/net/declaration/
---
{{% alert color="primary" %}} 

通常，所有 Aspose .NET 组件都需要设置完全信任权限。原因是 Aspose for .NET 组件需要访问注册表设置，虚拟目录以外的系统文件，以进行某些操作，如解析字体等。此外，Aspose for .NET 组件 (包括 Aspose.3D for .NET) 基于核心 .NET 系统类，在许多情况下也需要设置完全信任权限。

{{% /alert %}} 
##  **部分信任/中等信任挑战**
托管来自不同公司的多个应用程序的Internet服务提供商大多实施中等信任安全级别。此外，有时您需要在共享服务器上托管多个应用程序，例如在ISP或其他方案中，您必须使用中等信任级别来约束应用程序。ASP .NET 中等信任级别提供了一个受约束的执行环境，适用于隔离ISP服务器上承载的多个应用程序。在 .NET 2.0的情况下，此类安全级别可能会设置以下约束，这些约束可能会影响 Aspose.3D for .NET 正常执行的能力，例如:

- **Registrybermission不可用**。这意味着您无法访问注册表，这是在呈现电子表格或其他文档时枚举已安装字体所必需的。
- **FileIOPermission受限制**。这意味着您只能访问应用程序的虚拟目录层次结构中的文件。
##  **在中等信任权限集上使用 Aspose.3D for .NET**
您可以按照一些建议在中等信任级别或共享服务器环境中运行 Aspose.3D for .NET:

- 要在代码中设置许可证文件，最好在将许可证文件获取到流之后调用license.SetLicense(Stream) 方法。

请参见以下演示如何在中等信任模式下使用/运行 Aspose.3D for .NET 的示例。

{{< highlight "csharp" >}}

 // Instantiate the License object

Aspose.ThreeD.License lic = new Aspose.ThreeD.License();

// Get the license file into stream

FileStream stream = new FileStream("Aspose._3D.lic", FileMode.Open);

// Set the License stream

lic.SetLicense(stream);

// Close the stream

stream.Close();

//Open the template file

Scene scene = new Scene("test.obj");

// Save the OBJ file

scene.Save("dest.obj", FileFormat.WavefrontOBJ);



{{< /highlight >}}





