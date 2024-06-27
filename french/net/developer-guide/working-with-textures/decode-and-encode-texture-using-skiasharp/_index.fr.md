---
title: Décoder et encoder la texture à l'aide de SkiaSharp
type: docs
weight: 9
url: /fr/net/decode-and-encode-texture-using-skiasharp
description: Décoder la texture des fichiers image à l'aide de SkiaSharp
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs utilisent des encodeurs et des décodeurs d'image externes pour charger des textures ou enregistrer des textures dans différents formats d'image.

{{% /alert %}}


##  **Utilisez le code suivant pour définir un codec de texture de SkiaSharp**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **Enregistrez-le dans Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


Lorsque ce codec a été enregistré, tous les formats d'image supportés par SkiaSharp peuvent être utilisés dans TextureData.Save.





