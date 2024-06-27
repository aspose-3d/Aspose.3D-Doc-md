---
title: Textur mithilfe von ImageS harp decodieren und codieren
type: docs
weight: 11
url: /de/net/decode-and-encode-texture-using-imagesharp
description: Mit ImageS harp Textur aus Bilddateien decodieren
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) verwenden Entwickler externe Bildcodierer und-decoder, um Texturen zu laden oder Texturen in verschiedene Bildformate zu speichern.

{{% /alert %}}

##  **Implemen tieren Sie einen Textur-Codec mit ImageS harp**

Verwenden Sie die folgende Klasse, um Textur-Encoder und Textur-Decoder zu definieren:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


##  **Registrieren Sie es bei Aspose.3D**

Jetzt registrieren wir es in Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{< /highlight >}}


Wenn dieser Codec registriert wurde, können alle von ImageS harp unterstützten Bildformate in Texture Data.Save verwendet werden.

