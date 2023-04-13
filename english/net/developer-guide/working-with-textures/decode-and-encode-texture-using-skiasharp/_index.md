---
title: Decode and encode texture using SkiaSharp
type: docs
weight: 9
url: /net/decode-and-encode-texture-using-skiasharp
description: Decode texture from image files using SkiaSharp
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers use external image encoder and decoders to load textures or save textures into different image formats.

{{% /alert %}}


## **Use the following code to define a texture codec from SkiaSharp**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



## **Register it into Aspose.3D**

{{<highlight csharp>}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{</highlight>}}


When this codec has been registered, all SkiaSharp supported image formats can be used in TextureData.Save.





