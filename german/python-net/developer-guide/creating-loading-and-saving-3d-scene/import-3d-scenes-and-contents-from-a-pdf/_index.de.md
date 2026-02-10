---
title: Importieren Sie 3D Szenen und Inhalte aus einem PDF
type: docs
weight: 50
url: /de/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: Die Scene-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können 3D Szenen und Inhalte aus einer PDF-Datei extrahieren.
---
{{% alert color="primary" %}}

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können 3D Szenen und Inhalte aus einer PDF-Datei extrahieren.

{{% /alert %}}
##  **Offene Szene aus einem Passwort geschützt PDF**
Die `open`-Methode der `Scene`-Klasse erlaubt es, die 3D-Szene aus einer Eingabe-PDF-Datei zu laden. Entwickler können auch ein Passwort für die geschützten PDFs anwenden, indem sie die [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions)-Klasse verwenden, wie in diesem Code beispiel gezeigt:

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
##  **Extrahieren Sie alle Roh-3D-Inhalte aus einem PDF**
Die `extract`-Methode der [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)-Klasse ermöglicht es, 3D-Inhalte aus einer PDF-Datei zu extrahieren. Entwickler können den Inhalt durchgehen und ihn in den separaten Dateien speichern, wie in diesem Code beispiel gezeigt:

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
##  **Extrahieren Sie alle 3D-Szenen und speichern Sie sie in unterstützten 3D-Formaten**
Die `extract_scene`-Methode der `PdfFormat`-Klasse ermöglicht es, 3D-Szenen aus einer PDF-Datei zu extrahieren. Entwickler können die Szenen durchgehen und sie in den unterstützten 3D-Dateiformaten speichern, wie in diesem Code beispiel gezeigt:

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

Alle unterstützten 3D-Dateiformate sind auf der [Produkt übersicht](/3d/de/python-net/product-overview/)-Seite aufgeführt.

{{% /alert %}}
