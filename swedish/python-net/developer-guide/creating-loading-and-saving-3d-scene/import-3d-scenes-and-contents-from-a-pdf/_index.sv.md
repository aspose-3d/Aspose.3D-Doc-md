---
title: Importera 3D Scener och innehåll från en PDF
type: docs
weight: 50
url: /sv/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: Scenklassen för Aspose.3D API representerar en 3D scen. Utvecklare kan extrahera 3D scener och innehåll från en PDF-fil.
---
{{% alert color="primary" %}}

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) för Aspose.3D API representerar en 3D scen. Utvecklare kan extrahera 3D scener och innehåll från en PDF-fil.

{{% /alert %}}
##  **Open Scene from a Password Protected PDF**
`open`-metoden för `Scene`-klassen tillåter att ladda 3D-scenen från en inmatningsfil PDF. Utvecklare kan också använda lösenord för de skyddade PDF-filerna med [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) klassen som visas i detta exempel:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
##  **Extrahera alla obehandlade 3D Innehåll från en PDF**
`extract`-metoden för [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)-klassen gör det möjligt att dra ut 3D innehåll från en PDF-fil. Utvecklare kan itera igenom innehållet, och spara dem i de separata filerna som visas i detta kodexempel:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
##  **Extrahera alla 3D Scener och spara dem i format som stöds 3D**
`extract_scene`-metoden för `PdfFormat`-klassen tillåter att extrahera 3D scener från en PDF-fil. Utvecklare kan itera genom scenerna, och spara dem i de 3D filformat som stöds som visas i det här kodexemplet:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

All the supported 3D file formats are listed in the [Product Overview](/3d/python-net/product-overview/) page.

{{% /alert %}}
