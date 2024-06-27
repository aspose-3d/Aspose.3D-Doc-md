---
title: 使用SkiaSharp解码和编码纹理
type: docs
weight: 9
url: /zh/net/decode-and-encode-texture-using-skiasharp
description: 使用SkiaSharp从图像文件解码纹理
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员使用外部图像编码器和解码器来加载纹理或将纹理保存为不同的图像格式。

{{% /alert %}}


##  **使用以下代码从SkiaSharp定义纹理编解码器**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **将其注册到 Aspose。3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


注册此编解码器后，所有SkiaSharp支持的图像格式都可以在TextureData.Save中使用。





