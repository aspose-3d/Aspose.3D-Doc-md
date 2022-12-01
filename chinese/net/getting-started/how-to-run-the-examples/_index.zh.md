---
title: 如何运行示例
type: docs
weight: 70
url: /zh/net/how-to-run-the-examples/
description: 在这里，我们将指导您如何运行Aspose.3D for .NET的示例。
---
## **软件要求**
在下载和运行示例之前，请确保您满足以下要求。

1. Visual Studio 2010或更高
1. NuGet软件包管理器安装在Visual Studio中。确保Visual Studio中安装了最新的NuGet API版本。有关如何安装NuGet软件包管理器的详细信息，请检查<https://docs.microsoft.com/en-us/nuget/install-nuget-client-tools>
1. 转到工具-> 选项->NuGet包管理器-> 包源，并确保该选项**nuget.org**已检查
1. 示例项目使用NuGet自动包还原功能，因此您应该具有活动的internet连接。如果要执行示例的计算机上没有活动的internet连接，请检查[安装](/3d/zh/net/installation/)并在示例项目中手动添加对Aspose.3D.dll的引用。
## **从GitHub下载**
Aspose.3D for .NET的所有示例都托管在[GitHub](https://github.com/aspose-3d/Aspose.3D-for-.NET)。

- 您可以使用您最喜欢的GitHub客户端克隆存储库，也可以从以下位置下载ZIP文件[这里](https://github.com/aspose-3d/Aspose.3D-for-.NET/archive/master.zip)。
- 将ZIP文件的内容提取到计算机上的任何文件夹中。所有示例都位于`Examples`文件夹中。
- 项目中有一个解决方案文件，其中包含C#示例。
- 项目是在Visual Studio 2013中创建的，但解决方案文件与Visual Studio 2010 SP1和更高版本兼容。
- 在Visual Studio中打开解决方案文件并构建项目。
- 第一次运行时，依赖项将通过NuGet自动下载。
- `Examples`的根文件夹中的`Data`文件夹包含CSharp示例使用的输入文件。您必须与examples项目一起下载`Data`文件夹。
- 打开`RunExamples.cs`文件，所有的例子都是从这里调用的。
- 取消注释要从项目中运行的示例。

如果您在设置或运行示例时遇到任何问题，请随时使用我们的论坛与我们联系。
## **贡献**
如果您想添加或改进示例，我们鼓励您为该项目做出贡献。此存储库中的所有示例和展示项目都是开源的，可以在您自己的应用程序中自由使用。

要做出贡献，您可以分叉存储库，编辑源代码并创建拉取请求。如果发现有帮助，我们将检查更改并将其包含在存储库中。
