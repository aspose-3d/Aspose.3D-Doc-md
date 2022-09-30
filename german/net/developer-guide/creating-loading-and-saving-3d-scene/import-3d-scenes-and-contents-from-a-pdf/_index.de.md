---
title: Importieren Sie 3D Szenen und Inhalte aus einer PDF in C#
linktitle: Import 3D Szenen und Inhalt von einem PDF
type: docs
weight: 50
url: /de/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Die Szene klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können Szenen und Inhalte von 3D aus einer Datei PDF extrahieren.
---
{{% alert color="primary" %}}

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können 3D Szenen und Inhalte aus einer PDF-Datei extrahieren.

{{% /alert %}}
## **Offene Szene aus einem Passwort geschützt PDF**
Die `Open`-Methode der `Scene`-Klasse ermöglicht das Laden der 3D-Szene aus einer Eingabedatei PDF. Entwickler können auch ein Passwort für die geschützten PDFs unter Verwendung der [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions)-Klasse anwenden, wie in diesem Code beispiel C# gezeigt:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
## **Extrahieren Sie alle Roh-Inhalte 3D aus einem PDF**
Die Extract-Methode der [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)-Klasse ermöglicht es, 3D-Inhalte aus einer PDF-Datei zu extrahieren. Entwickler können den Inhalt durchgehen und ihn in den separaten Dateien speichern, wie in diesem Code beispiel C# gezeigt:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
## **Extrahieren Sie alle Szenen 3D und speichern Sie sie in unterstützte 3D Formate**
Die `ExtractScene`-Methode der `PdfFormat`-Klasse ermöglicht das Extrahieren von 3D-Szenen aus einer PDF-Datei. Entwickler können die Szenen durchgehen und sie in den unterstützten 3D-Dateiformaten speichern, wie in diesem Code beispiel C# gezeigt:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

Alle unterstützten 3D Dateiformate sind in der[Produkt übersicht](/3d/de/net/product-overview/)Seite.

{{% /alert %}}
