---
title: Textur mithilfe von System.Drawing decodieren und codieren
type: docs
weight: 7
url: /de/net/decode-and-encode-texture-using-system-drawing
description: Textur aus Bilddateien mithilfe von System. Zeichnung decodieren
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) verwenden Entwickler externe Bildcodierer und-decoder, um Texturen zu laden oder Texturen in verschiedene Bildformate zu speichern.

{{% /alert %}}

##  **Implemen tieren Sie einen Textur-Codec mithilfe von System.Drawing**

Verwenden Sie die folgende Klasse, um Textur-Encoder und Textur-Decoder zu definieren:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **Registrieren Sie es bei Aspose.3D**

Jetzt registrieren wir es in Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


Wenn dieser Codec registriert wurde, können alle von System.Drawing unterstützten Bildformate in Texture Data.Save verwendet werden.

