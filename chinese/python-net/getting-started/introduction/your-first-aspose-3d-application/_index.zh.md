---
title: 你的第一个 Aspose.3D 应用程序
type: docs
weight: 30
url: /zh/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

本教程介绍如何使用 Aspose.3D 简单的 API 创建您的第一个应用程序。该简单应用程序会在指定的 3D 场景中创建一个 3d 文件。

{{% /alert %}}

## **如何创建应用程序**

以下步骤使用 Aspose.3D API 创建应用程序：

1. 创建 [Scene](https://reference.aspose.com/3d/zh/python-net/aspose.threed/scene/) 类的实例。
1. 如果您有许可证，请[应用许可证](/3d/zh/python-net/licensing/)。
   如果您使用的是评估版，请跳过与许可证相关的代码 行。
1. 创建新的 3D 文件，或打开现有的 3D 文件。
1. 访问 3D 文件中的场景内容。
1. 生成修改后的 3D 文件。

以上步骤的实现将在下面的示例中演示。

### **如何创建新的场景文档**

以下示例从头开始创建一个新的 3D 场景文件。首先，创建一个 3D 场景，然后将文件以 FBX 格式保存。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}

### **如何打开现有文件**

以下示例打开名为 "document.fbx" 的现有 3D 模板文件。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
