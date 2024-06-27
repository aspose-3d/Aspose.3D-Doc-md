---
title: Decodificare e codificare la texture utilizzando System.Drawing
type: docs
weight: 7
url: /it/net/decode-and-encode-texture-using-system-drawing
description: Decodificare la texture dai file di immagine utilizzando System.Drawing
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori utilizzano codificatori e decodificatori di immagini esterni per caricare trame o salvare trame in diversi formati di immagine.

{{% /alert %}}

##  **Implementare un codec texture utilizzando System.Drawing**

Utilizzare la seguente classe per definire codificatori texture e decodificatore texture:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **Registralo in Aspose.3D**

Ora registriamolo in Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


Quando questo codec è stato registrato, tutti i formati di immagine supportati da System.Drawing possono essere utilizzati in TextureData.Save.

