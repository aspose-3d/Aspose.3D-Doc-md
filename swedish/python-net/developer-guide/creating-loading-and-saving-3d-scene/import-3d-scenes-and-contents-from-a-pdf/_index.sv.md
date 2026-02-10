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

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import PdfLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a new scene
scene = Scene()
options = PdfLoadOptions()
options.password = "password".encode("utf-8")
#  Use loading options and apply password
opt = options
#  Open scene
scene.open("data-dir"  + "House_Design.pdf", opt)

{{< /highlight >}}
##  **Extrahera alla obehandlade 3D Innehåll från en PDF**
`extract`-metoden för [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)-klassen gör det möjligt att dra ut 3D innehåll från en PDF-fil. Utvecklare kan itera igenom innehållet, och spara dem i de separata filerna som visas i detta kodexempel:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
password = None
#  Extract 3D contents
contents = FileFormat.PDF.extract("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the contents and in separate 3D files
for content in contents:
    fileName = "3d-"  + str(i)
    i = i + 1
    with open(fileName, "wb") as f:
        f.write(content)

{{< /highlight >}}
##  **Extrahera alla 3D Scener och spara dem i format som stöds 3D**
`extract_scene`-metoden för `PdfFormat`-klassen tillåter att extrahera 3D scener från en PDF-fil. Utvecklare kan itera genom scenerna, och spara dem i de 3D filformat som stöds som visas i det här kodexemplet:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
password = None
scenes = FileFormat.PDF.extract_scene("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the scenes and save in 3D files
for scene in scenes:
    fileName = "3d-"  + str(i) + ".fbx"
    i = i + 1
    scene.save("out"  + fileName, FileFormat.FBX7400ASCII)

{{< /highlight >}}

{{% alert color="primary" %}}

All the supported 3D file formats are listed in the [Product Overview](/3d/python-net/product-overview/) page.

{{% /alert %}}
