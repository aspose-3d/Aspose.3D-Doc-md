---
title: Importera 3D Scener och innehåll från en PDF i C#
linktitle: Importera 3D Scener och innehåll från en PDF
type: docs
weight: 50
url: /sv/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Scenklassen för Aspose.3D API representerar en 3D scen. Utvecklare kan extrahera 3D scener och innehåll från en PDF-fil.
---
{{% alert color="primary" %}}

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) för Aspose.3D API representerar en 3D scen. Utvecklare kan extrahera 3D scener och innehåll från en PDF-fil.

{{% /alert %}}
##  **Open Scene from a Password Protected PDF**
`Open`-metoden för `Scene`-klassen tillåter att ladda 3D-scenen från en inmatningsfil PDF. Utvecklare kan också använda lösenord för de skyddade PDF-filerna med [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) klassen som visas i detta C# kodexempel:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **Extrahera alla obehandlade 3D Innehåll från en PDF**
Utdragsmetoden för [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) gör det möjligt att dra ut 3D innehåll från en PDF-fil. Utvecklare kan itera genom innehållet, och spara dem i de separata filerna som visas i detta C# kodexempel:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **Extrahera alla 3D Scener och spara dem i format som stöds 3D**
`ExtractScene`-metoden för `PdfFormat`-klassen tillåter att extrahera 3D scener från en PDF-fil. Utvecklare kan itera genom scenerna, och spara dem i de 3D filformat som stöds som visas i detta C# kodexempel:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

All the supported 3D file formats are listed in the [Product Overview](/3d/net/product-overview/) page.

{{% /alert %}}
