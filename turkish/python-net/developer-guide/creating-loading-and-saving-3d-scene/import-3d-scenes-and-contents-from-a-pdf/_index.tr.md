---
title: 3D sahnelerini ve içeriğini PDF 'dan içe aktarın
type: docs
weight: 50
url: /tr/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.
---
{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.

{{% /alert %}}
##  **Bir şifre korumalı PDF açık sahne**
`Scene` sınıfının `open` yöntemi, 3D sahnesini bir giriş PDF dosyasından yüklemeye izin verir. Geliştiriciler ayrıca bu kod örneğinde gösterildiği gibi [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) sınıfını kullanarak korunan pdf'ler için şifre de uygulayabilir:

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
##  **Tüm ham 3D içeriğini PDF 'dan ayıklayın**
The `extract` method of the [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) class allows to extract 3D contents from a PDF file. Developers may iterate through the contents, and save them into the separate files as shown in this code example:

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
##  **Extract All 3D Scenes and Save them into Supported 3D Formats**
`PdfFormat` sınıfının `extract_scene` yöntemi, PDF dosyasından 3D sahnelerini çıkarmanıza izin verir. Geliştiriciler sahneler aracılığıyla yineleyebilir ve bu kod örneğinde gösterildiği gibi desteklenen 3D dosya formatlarında kaydedebilir:

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

Desteklenen tüm 3D dosya biçimleri [Product Overview](/3d/tr/python-net/product-overview/) sayfasında listelenir.

{{% /alert %}}
