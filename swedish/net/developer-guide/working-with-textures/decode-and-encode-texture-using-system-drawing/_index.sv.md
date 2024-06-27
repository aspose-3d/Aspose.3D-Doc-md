---
title: Avkoda och koda textur med hjälp av System.Drawing
type: docs
weight: 7
url: /sv/net/decode-and-encode-texture-using-system-drawing
description: Avkoda textur från bildfiler med hjälp av System.Drawing
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) använder utvecklare externa bildkodare och avkodare för att ladda texturer eller spara texturer i olika bildformat.

{{% /alert %}}

##  **Implementera en textur codec med hjälp av System.Drawing**

Använd följande klass för att definiera texturkodare och texturdekodare:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **Registrera den till Aspose.3D**

Now let's register it into Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


När denna codec har registrerats, kan alla System.Rita bildformat som stöds användas i TextureData.Save.

