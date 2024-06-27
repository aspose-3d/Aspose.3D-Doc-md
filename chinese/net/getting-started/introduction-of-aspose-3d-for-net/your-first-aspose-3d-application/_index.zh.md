---
title: 您的第一个 Aspose.3D 应用程序
type: docs
weight: 30
url: /zh/net/your-first-aspose-3d-application/
description: 使用 Aspose.3D for .NET 以任何受支持的格式创建、编辑和保存您的第一个3d文件，以 C# 体验其简单性和强大功能。
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

本教程介绍如何使用 Aspose.3D 的简单 API 创建您的第一个应用程序。这个简单的应用程序在指定的 3D 场景中创建一个3d文件。

{{% /alert %}}

##  **如何创建应用程序**

以下步骤使用 Aspose.3D API 创建应用程序:

1. 创建 [场景](https://reference.aspose.com/3d/net/aspose.threed/scene/) 类的实例。
1. 如果您有许可证，则为 [应用它](/3d/zh/net/licensing/)。
如果您使用的是评估版，请跳过与许可证相关的代码行。
1. 创建新的 3D 文件，或打开现有的 3D 文件。
1. 访问 3D 文件中的场景内容。
1. 生成修改后的 3D 文件。

上述步骤的实现在下面的实施例中演示。

###  **如何新建场景文档**

下面的示例从头开始创建一个新的 3D 场景文件。首先，创建一个 3D 场景，然后以 FBX 格式保存文件。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

###  **如何打开现有文件**

下面的示例打开名为 “document.fbx” 的现有 3D 模板文件，然后将 3D 场景或文档以各种支持的 3D 格式保存到流中。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Save3DScene.cs" >}}
