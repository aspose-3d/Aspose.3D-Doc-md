---
title: 如何在Blazor中运行 Aspose.3D
type: docs
weight: 138
url: /zh/net/how-to-run-aspose-3d-in-blazor/
description: 了解如何在Blazor中运行 Aspose.3D。
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## 概述

Blazor是由 Microsoft 开发的web应用程序框架，它允许使用 C# 和 .NET 编写客户端web应用程序。Blazor的特点是使用WebAssembly技术，该技术使在浏览器中运行的应用程序能够使用高性能的本机代码。Blazor采用组件化架构，允许开发人员将UI划分为独立的组件，从而实现代码的可重用性和可维护性。Blazor支持跨平台开发，可以在各种现代浏览器和设备上运行，包括桌面、移动和嵌入式设备。

通常，Blazor提供了一种构建web应用程序的现代方法，使开发人员能够在浏览器中使用 C# 和 .NET 技术构建高性能、交互式和可维护的web应用程序。

## 第一个包含 Aspose.3D 的Blazor应用程序

在此示例中，我们创建了一个简单的Blazor服务器应用程序，创建了一个3d文件，并截取了文件内容的屏幕截图并将其显示在网页上。在项目创建过程中，我们可以根据自己的需要进行配置，例如检查 “启用Docker” 选项，以便可以在Docker中构建和运行Blazor应用程序。

### 创建第一个Blazor应用程序

让我们以VS2022工具为例，使用 Aspose 创建第一个blazor应用程序。3D，请按照以下步骤操作:
1. 选择File ->New ->Project，然后使用blazer关键字进行筛选以选择相应的项目模板。
<br>
<img src="1.png" width=80% />
1. 将项目名称设置为 “BlazorTest” 并选择路径。
<br>
<img src="2.png" width=80% />
1. 配置项目中使用的库和其他选项。最后，点击 “创建” 按钮生成您的第一个blazer项目。
<br>
<img src="3.png" width=80% />
1. 进入项目后，单击项目下的 “依赖项”，然后选择 “管理 NuGet 包...” 以添加 Aspose.3D 库。
<br>
<img src="4.png" width=80% />
1. 输入用于筛选的关键字并安装最新的 Aspose.3D 库。
<br>
<img src="5.png" width=80% />
1. 双击 “Index.razor” 文件以编辑和导入所需的库。添加一些数据和图片。
<br>
<img src="5.png" width=80% />
1. 编译并运行该项目，您将获得以下结果。
<br>
<img src="7.png" width=80% />

### 第一个Blazor应用程序中的示例代码

下面的示例代码包含在Index.razor文件中:
```
@page "/"
@using Aspose.ThreeD;
@using Aspose.ThreeD.Entities;
@using Aspose.ThreeD.Utilities;

<PageTitle>Index</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<SurveyPrompt Title="How is Blazor working for you?" />

<img src="@imageUrl" />

@code
{
    private string imageUrl="https://docs.aspose.com/3d/net/working-with-cylinder/working-with-cylinder_1.png";

    public Index()
    {
        CreateFile();
    }

    private void CreateFile()
    {
        // Create a scene
        Scene scene = new Scene();

        // Initialize cylinder
        var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

        // Set OffsetTop
        cylinder1.OffsetTop = new Vector3(5, 3, 0);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

        // Intialze second cylinder without customized OffsetTop
        var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder2);

        // Save
        scene.Save("CustomizedOffsetTopCylinder.obj");
    }
}

```