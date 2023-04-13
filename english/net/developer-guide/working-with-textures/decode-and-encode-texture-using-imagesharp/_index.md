---
title: Decode and encode texture using ImageSharp
type: docs
weight: 11
url: /net/decode-and-encode-texture-using-imagesharp
description: Decode texture from image files using ImageSharp
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers use external image encoder and decoders to load textures or save textures into different image formats.

{{% /alert %}}

## **Implement a texture codec using ImageSharp**

Use the following class to define texture encoders and texture decoder:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


## **Register it into Aspose.3D**

Now let's register it into Aspsoe.3D:

{{<highlight csharp>}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{</highlight>}}


When this codec has been registered, all ImageSharp supported image formats can be used in TextureData.Save.

