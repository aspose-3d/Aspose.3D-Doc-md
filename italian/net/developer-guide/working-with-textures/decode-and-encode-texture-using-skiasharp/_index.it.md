---
title: Decodificare e codificare la texture utilizzando SkiaSharp
type: docs
weight: 9
url: /it/net/decode-and-encode-texture-using-skiasharp
description: Decodificare la trama dai file immagine utilizzando SkiaSharp
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori utilizzano codificatori e decodificatori di immagini esterni per caricare trame o salvare trame in diversi formati di immagine.

{{% /alert %}}


##  **Utilizzare il codice seguente per definire un codec texture da SkiaSharp**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **Registralo in Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


Quando questo codec è stato registrato, tutti i formati di immagine supportati da SkiaSharp possono essere utilizzati in TextureData.Save.





