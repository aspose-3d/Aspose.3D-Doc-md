---
title: 自定义 FBX 文件中的RotationOrder
type: docs
weight: 10
url: /zh/net/customize-rotation-order-in-fbx-file
description: 使用 Aspose.3D for .NET，开发人员可以定义自定义本机 FBX 属性，如RotationOrder。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/) 时，开发人员有时需要对特定于格式的功能进行精细控制，例如更改 FBX 导出器中的 `RotationOrder`。虽然可能没有公开的 API 直接公开此功能，但 Aspose.3D for .NET 提供了通过其灵活的体系结构实现此类自定义的方法。
{{% /alert %}}



以下是如何在 Aspose 中处理此问题。3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

在这个例子中:

1. 从 RVM 文件创建场景。
1. 访问场景中的所有节点。
1. Set custom property: SetProperty方法用于设置 `RotationOrder` 属性，演示如何利用内部机制来控制公共 API 未直接公开的格式特定功能。
1. 保存场景: 使用自定义的 `RotationOrder` 保存场景。

通过使用这些技术，Aspose.3D 允许开发人员微调和控制 3D 格式的特定功能，确保在各种 3D 应用程序中满足详细和精确的要求。