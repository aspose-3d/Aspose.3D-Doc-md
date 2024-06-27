---
title: Decodificare e codificare la texture utilizzando ImageSharp
type: docs
weight: 11
url: /it/net/decode-and-encode-texture-using-imagesharp
description: Decodificare la trama dai file immagine utilizzando ImageSharp
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori utilizzano codificatori e decodificatori di immagini esterni per caricare trame o salvare trame in diversi formati di immagine.

{{% /alert %}}

##  **Implementare un codec texture utilizzando ImageSharp**

Utilizzare la seguente classe per definire codificatori texture e decodificatore texture:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


##  **Registralo in Aspose.3D**

Ora registriamolo in Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{< /highlight >}}


Quando questo codec è stato registrato, tutti i formati di immagine supportati da ImageSharp possono essere utilizzati in TextureData.Save.

