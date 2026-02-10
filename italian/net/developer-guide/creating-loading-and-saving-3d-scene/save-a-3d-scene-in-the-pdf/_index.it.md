---
title: Salva una scena di 3D in PDF in C#
linktitle: Salva una scena di 3D in PDF
type: docs
weight: 60
url: /it/net/save-a-3d-scene-in-the-pdf/
description: La classe Scena di Aspose.3D API rappresenta una scena di 3D. Gli sviluppatori possono creare una scena da 3D aggiungendo fotocamera, luce, poligoni e varie altre entità. Ora possono anche salvare una scena di 3D nel formato di file PDF.
---
##  **Panoramica**

Questo articolo spiega come è possibile convertire il file 3D in formato PDF utilizzando C# .NET 3D di manipolazione e conversione di file API, prima devi [Caricare il file 3D nell'oggetto Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) e poi salvarlo in formato PDF. Copre un'ampia gamma di argomenti, ad es.

- Convertire 3D in PDF in C#
- Convertire FBX in PDF in C#
- Convertire STL in PDF in C#
- Convertire U3D in PDF in C#
- Convertire OBJ in PDF in C#

{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) di Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono creare una scena da 3D aggiungendo fotocamera, luce, poligoni e varie altre entità. Ora possono anche salvare una scena di 3D nel formato di file PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET scrive direttamente le informazioni relative a API e al numero di versione nei documenti di output. Ad esempio, dopo il rendering di un disegno a PDF, Aspose.3D for .NET popola il campo `Application` con valore 'Aspose. Campo 3D 'e `PDF Producer` con valore, e.g' Aspose.3D 17,9 '.

Tieni presente che non puoi istruire Aspose.3D for .NET API per modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}} 
##  **Crea 3D PDF con un cilindro e renderizzato in modalità illustrazione ombreggiata con illuminazione ottimizzata CAD**
Il metodo Salva della classe `Scene` consente di salvare una scena 3D nel formato PDF. Gli sviluppatori possono caricare qualsiasi file supportato da 3D o creare una nuova scena 3D, possono salvare una scena 3D nel formato PDF come mostrato in questo esempio di codice C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a new scene
            Scene scene = new Scene();
            // Create a cylinder child node
            scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan) };
            // Set rendering mode and lighting scheme
            PdfSaveOptions opt = new PdfSaveOptions();
            opt.LightingScheme = PdfLightingScheme.CAD;
            opt.RenderMode = PdfRenderMode.ShadedIllustration;
            // Save in the PDF format
            scene.Save("output_out.pdf", opt);

{{< /highlight >}}
