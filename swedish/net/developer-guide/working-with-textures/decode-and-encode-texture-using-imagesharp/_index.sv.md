---
title: Avkoda och koda textur med ImageSharp
type: docs
weight: 11
url: /sv/net/decode-and-encode-texture-using-imagesharp
description: Avkoda textur från bildfiler med ImageSharp
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) använder utvecklare externa bildkodare och avkodare för att ladda texturer eller spara texturer i olika bildformat.

{{% /alert %}}

##  **Implementera en textur codec med ImageSharp**

Använd följande klass för att definiera texturkodare och texturdekodare:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


##  **Registrera den till Aspose.3D**

Now let's register it into Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{< /highlight >}}


När denna codec har registrerats kan alla ImageSharp stödda bildformat användas i TextureData.Save.

