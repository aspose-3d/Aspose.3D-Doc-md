---
title: Import 3D Scenes and Contents from a PDF
type: docs
weight: 50
url: /python-net/import-3d-scenes-and-contents-from-a-pdf/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.
---

{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.

{{% /alert %}}
## **Open Scene from a Password Protected PDF**
The `open` method of the `Scene` class allows to load the 3D scene from an input PDF file. Developers may also apply password for the protected PDFs using [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) class as shown in this code example:

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
## **Extract All Raw 3D Contents from a PDF**
The `extract` method of the [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) class allows to extract 3D contents from a PDF file. Developers may iterate through the contents, and save them into separate files as shown in this code example:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
password = None
#  Extract 3D contents
contents = FileFormat.PDF.extract("data-dir" + "House_Design.pdf", password)
i = 1
#  Iterate through contents and save in separate 3D files
for content in contents:
    fileName = "3d-" + str(i)
    i = i + 1
    with open(fileName, "wb") as f:
        f.write(content)
{{< /highlight >}}
## **Extract All 3D Scenes and Save them into Supported 3D Formats**
The `extract_scene` method of the `PdfFormat` class allows to extract 3D scenes from a PDF file. Developers may iterate through the scenes, and save them in supported 3D file formats as shown in this code example:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
password = None
scenes = FileFormat.PDF.extract_scene("data-dir" + "House_Design.pdf", password)
i = 1
#  Iterate through scenes and save in 3D files
for scene in scenes:
    fileName = "3d-" + str(i) + ".fbx"
    i = i + 1
    scene.save("out" + fileName, FileFormat.FBX7400ASCII)
{{< /highlight >}}

{{% alert color="primary" %}}

All the supported 3D file formats are listed in the [Product Overview](/3d/python-net/product-overview/) page.

{{% /alert %}}
