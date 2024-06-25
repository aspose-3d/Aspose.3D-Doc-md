---
title: Importar 3D escenas y contenidos de un PDF en C#
linktitle: Importar 3D escenas y contenidos desde un PDF
type: docs
weight: 50
url: /es/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: La clase Scene de Aspose.3D API representa una escena 3D. Los desarrolladores pueden extraer 3D escenas y contenidos de un archivo PDF.
---
{{% alert color="primary" %}}

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la Aspose.3D API representa una escena 3D. Los desarrolladores pueden extraer 3D escenas y contenidos de un archivo PDF.

{{% /alert %}}
##  **Abrir escena desde una contraseña protegida PDF**
El método `Open` de la clase `Scene` permite cargar la escena 3D desde un archivo PDF de entrada. Los desarrolladores también pueden aplicar una contraseña para los PDF protegidos usando la clase [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) como se muestra en este ejemplo de código C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **Extraer todo el contenido Raw 3D de un PDF**
El método Extract de la clase [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permite extraer el contenido 3D de un archivo PDF. Los desarrolladores pueden iterar a través de los contenidos y guardarlos en los archivos separados como se muestra en este ejemplo de código C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **Extraer todas las escenas 3D y guardarlas en formatos 3D compatibles**
El método `ExtractScene` de la clase `PdfFormat` permite extraer escenas 3D de un archivo PDF. Los desarrolladores pueden iterar a través de las escenas y guardarlas en los formatos de archivo 3D compatibles como se muestra en este ejemplo de código C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

Todos los formatos de archivo 3D admitidos se enumeran en la página [Descripción general del producto](/3d/es/net/product-overview/).

{{% /alert %}}
