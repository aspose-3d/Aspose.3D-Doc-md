---
title: Importa 3D scene e contenuti da PDF
type: docs
weight: 50
url: /it/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: La classe Scena di Aspose.3D API rappresenta una scena di 3D. Gli sviluppatori possono estrarre 3D scene e contenuti da un file PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) di Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono estrarre 3D scene e contenuti da un file PDF.

{{% /alert %}}
##  **Apri la scena da una password protetta PDF**
Il metodo `open` della classe `Scene` consente di caricare la scena 3D da un file PDF inserito. Gli sviluppatori possono anche applicare la password per i PDF protetti utilizzando la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) come mostrato in questo esempio di codice:

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
##  **Estrai tutti i contenuti Raw 3D da PDF**
Il metodo `extract` della classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) consente di estrarre 3D contenuti da un file PDF. Gli sviluppatori possono scorrere i contenuti e salvarli nei file separati come mostrato in questo esempio di codice:

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
##  **Estrai tutte le scene da 3D e salvale in formati 3D supportati**
Il metodo `extract_scene` della classe `PdfFormat` consente di estrarre 3D scene da un file PDF. Gli sviluppatori possono scorrere le scene e salvarle nei formati di file 3D supportati come mostrato in questo esempio di codice:

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

Tutti i formati di file 3D supportati sono elencati nella pagina [Panoramica del prodotto](/3d/it/python-net/product-overview/).

{{% /alert %}}
