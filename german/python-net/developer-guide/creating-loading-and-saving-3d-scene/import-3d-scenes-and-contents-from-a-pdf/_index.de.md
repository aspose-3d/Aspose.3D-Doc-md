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

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
##  **Extrahieren Sie alle Roh-3D-Inhalte aus einem PDF**
Die `extract`-Methode der [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)-Klasse ermöglicht es, 3D-Inhalte aus einer PDF-Datei zu extrahieren. Entwickler können den Inhalt durchgehen und ihn in den separaten Dateien speichern, wie in diesem Code beispiel gezeigt:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
##  **Extrahieren Sie alle 3D-Szenen und speichern Sie sie in unterstützten 3D-Formaten**
Die `extract_scene`-Methode der `PdfFormat`-Klasse ermöglicht es, 3D-Szenen aus einer PDF-Datei zu extrahieren. Entwickler können die Szenen durchgehen und sie in den unterstützten 3D-Dateiformaten speichern, wie in diesem Code beispiel gezeigt:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Alle unterstützten 3D-Dateiformate sind auf der [Produkt übersicht](/3d/de/python-net/product-overview/)-Seite aufgeführt.

{{% /alert %}}
