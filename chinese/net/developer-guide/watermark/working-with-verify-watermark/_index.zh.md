---
title: 验证水印
type: docs
weight: 170
url: /zh/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

使用 Aspose.3D for .NET API，开发人员可以轻松地为 3D 文件添加盲水印验证，并在保存为任何支持的输出文件格式时使用。

{{% /alert %}}
# **创建 3D 场景**
首先，您需要从 3D 文件创建 3D 场景。以下代码片段展示了如何使用此功能：

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **解码水印**
Aspose.3D for .NET 使用 `DecodeWatermark` 方法来确认填充密码后 3D 文件的水印。以下代码片段展示了如何使用此功能：

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithVerifyWatermark-DecodeWatermark.cs" >}}

# **文档确认**
对于返回的结果，如果返回结果为 null，则表示 3D 文档中没有添加水印。如果返回文本信息，则为 3D 文件的水印。如果密码输入错误，将返回错误消息。