---
title: Importa 3D scene e contenuti da PDF in C#
linktitle: Importa 3D scene e contenuti da PDF
type: docs
weight: 50
url: /it/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: La classe Scena di Aspose.3D API rappresenta una scena di 3D. Gli sviluppatori possono estrarre 3D scene e contenuti da un file PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) di Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono estrarre 3D scene e contenuti da un file PDF.

{{% /alert %}}
##  **Apri la scena da una password protetta PDF**
Il metodo `Open` della classe `Scene` consente di caricare la scena 3D da un file PDF inserito. Gli sviluppatori possono anche applicare la password per i PDF protetti utilizzando la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) come mostrato in questo esempio di codice C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **Estrai tutti i contenuti Raw 3D da PDF**
Il metodo Extract della classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) consente di estrarre 3D contenuti da un file PDF. Gli sviluppatori possono scorrere i contenuti e salvarli nei file separati come mostrato in questo esempio di codice C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **Estrai tutte le scene da 3D e salvale in formati 3D supportati**
Il metodo `ExtractScene` della classe `PdfFormat` consente di estrarre 3D scene da un file PDF. Gli sviluppatori possono scorrere le scene e salvarle nei formati di file 3D supportati come mostrato in questo esempio di codice C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

Tutti i formati di file 3D supportati sono elencati nella pagina [Panoramica del prodotto](/3d/it/net/product-overview/).

{{% /alert %}}
