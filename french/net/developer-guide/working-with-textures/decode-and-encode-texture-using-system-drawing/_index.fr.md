---
title: Décoder et encoder la texture à l'aide de System.Drawing
type: docs
weight: 7
url: /fr/net/decode-and-encode-texture-using-system-drawing
description: Décoder la texture des fichiers image à l'aide de System.Drawing
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs utilisent des encodeurs et des décodeurs d'image externes pour charger des textures ou enregistrer des textures dans différents formats d'image.

{{% /alert %}}

##  **Implémenter un codec de texture à l'aide de System.Drawing**

Utilisez la classe suivante pour définir les encodeurs de texture et le décodeur de texture:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **Enregistrez-le dans Aspose.3D**

Maintenant, enregistrons-le dans Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


Lorsque ce codec a été enregistré, tous les formats d'image pris en charge par System.Drawing peuvent être utilisés dans TextureData.Save.

