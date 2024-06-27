---
title: Decodificar y codificar textura usando System.Drawing
type: docs
weight: 7
url: /es/net/decode-and-encode-texture-using-system-drawing
description: Decodificar textura de archivos de imagen usando System.Drawing
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores usan codificadores y decodificadores de imágenes externos para cargar texturas o guardar texturas en diferentes formatos de imagen.

{{% /alert %}}

##  **Implemente un códec de textura usando System.Drawing**

Utilice la siguiente clase para definir los codificadores de textura y el decodificador de textura:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **Registrarlo en Aspose.3D**

Ahora vamos a registrarlo en Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


Una vez registrado este códec, todos los formatos de imagen compatibles con System.Drawing se pueden utilizar en TextureData.Save.

