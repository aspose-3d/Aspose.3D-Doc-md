---
title: 使用System.Drawing解码和编码纹理
type: docs
weight: 7
url: /zh/net/decode-and-encode-texture-using-system-drawing
description: 使用System.Drawing从图像文件中解码纹理
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员使用外部图像编码器和解码器来加载纹理或将纹理保存为不同的图像格式。

{{% /alert %}}

##  **使用System.Drawing实现纹理编解码器**

使用以下类定义纹理编码器和纹理解码器:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **将其注册到 Aspose。3D**

现在让我们将其注册到Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


注册此编解码器后，所有System.Drawing支持的图像格式都可以在TextureData.Save中使用。

