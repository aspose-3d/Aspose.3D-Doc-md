---
title: Textur mit SkiaS harp decodieren und codieren
type: docs
weight: 9
url: /de/net/decode-and-encode-texture-using-skiasharp
description: Mit SkiaS harp Textur aus Bilddateien decodieren
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) verwenden Entwickler externe Bildcodierer und-decoder, um Texturen zu laden oder Texturen in verschiedene Bildformate zu speichern.

{{% /alert %}}


##  **Verwenden Sie den folgenden Code, um einen Textur-Codec von SkiaS harp zu definieren**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **Registrieren Sie es bei Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


Wenn dieser Codec registriert wurde, können alle von SkiaS harp unterstützten Bildformate in Texture Data.Save verwendet werden.





