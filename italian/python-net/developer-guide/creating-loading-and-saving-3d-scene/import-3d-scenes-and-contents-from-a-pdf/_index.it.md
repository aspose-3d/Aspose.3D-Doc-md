---
title: Importazione 3D Scene e contenuti da un PDF
type: docs
weight: 50
url: /it/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: La classe Scena dello Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono estrarre 3D scene e contenuti da un file PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) dello Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono estrarre scene e contenuti 3D da un file PDF.

{{% /alert %}}
## **Scena aperta da una password protetta PDF**
Il metodo `open` della classe `Scene` consente di caricare la scena 3D da un file di input PDF. Gli sviluppatori possono anche applicare la password per i PDF protetti utilizzando la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) come mostrato in questo esempio di codice:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
## **Estrarre tutto il Raw 3D Contenuto da un PDF**
Il metodo `extract` della classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) consente di estrarre i contenuti 3D da un file PDF. Gli sviluppatori possono scorrere i contenuti e salvarli nei file separati come mostrato in questo esempio di codice:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
## **Estrarre tutte le scene 3D e salvarle in formati supportati 3D**
Il metodo `extract_scene` della classe `PdfFormat` consente di estrarre 3D scene da un file PDF. Gli sviluppatori possono scorrere le scene e salvarle nei formati di file 3D supportati come mostrato in questo esempio di codice:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Tutti i formati di file 3D supportati sono elencati nel[Panoramica del prodotto](/3d/it/python-net/product-overview/)Pagina.

{{% /alert %}}
