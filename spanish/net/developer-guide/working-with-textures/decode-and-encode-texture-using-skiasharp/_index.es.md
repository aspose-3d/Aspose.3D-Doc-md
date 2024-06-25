---
title: Decodificar y codificar textura usando SkiaSharp
type: docs
weight: 9
url: /es/net/decode-and-encode-texture-using-skiasharp
description: Decodificar la textura de los archivos de imagen usando SkiaSharp
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores usan codificadores y decodificadores de imágenes externos para cargar texturas o guardar texturas en diferentes formatos de imagen.

{{% /alert %}}


##  **Use el siguiente código para definir un códec de textura desde SkiaSharp**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **Registrarlo en Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


Una vez registrado este códec, todos los formatos de imagen compatibles con SkiaSharp se pueden utilizar en TextureData.Save.





