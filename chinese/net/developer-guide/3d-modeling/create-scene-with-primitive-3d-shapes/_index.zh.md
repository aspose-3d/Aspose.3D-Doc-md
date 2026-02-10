---
title: 创建具有原始 3D 形状的场景
type: docs
weight: 10
url: /zh/net/create-scene-with-primitive-3d-shapes/
description: 使用 Aspose.3D for .NET，开发人员可以定义具有原始 3D 形状的场景。所有参数化图元将自动转换为网格，同时以任何支持的输出文件格式保存。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员可以定义具有原始 3D 形状的场景。所有参数化图元将自动转换为网格，同时以任何支持的输出文件格式保存。

{{% /alert %}}
##  **从原始 3D 形状生成场景**
建模是纯粹的创建过程，Aspose.3D API 支持创建具有原始 3D 形状的场景。
###  **编程示例**
此代码示例创建一个包含原始 3D 形状的场景，并将其保存在 FBX 文件中。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
