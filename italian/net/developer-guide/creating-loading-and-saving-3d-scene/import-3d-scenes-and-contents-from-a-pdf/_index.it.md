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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Estrai tutti i contenuti Raw 3D da PDF**
Il metodo Extract della classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) consente di estrarre 3D contenuti da un file PDF. Gli sviluppatori possono scorrere i contenuti e salvarli nei file separati come mostrato in questo esempio di codice C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
byte[] password = null;
// Extract 3D contents
List<byte[]> contents = FileFormat.PDF.Extract("House_Design.pdf", password);
int i = 1;
// Iterate through the contents and in separate 3D files
foreach (byte[] content in contents)
{
    string fileName = "3d-" + (i++);
    File.WriteAllBytes(fileName, content);
}

{{< /highlight >}}
##  **Estrai tutte le scene da 3D e salvale in formati 3D supportati**
Il metodo `ExtractScene` della classe `PdfFormat` consente di estrarre 3D scene da un file PDF. Gli sviluppatori possono scorrere le scene e salvarle nei formati di file 3D supportati come mostrato in questo esempio di codice C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            byte[] password = null;
            List<Scene> scenes = FileFormat.PDF.ExtractScene("House_Design.pdf", password);
            int i = 1;
            // Iterate through the scenes and save in 3D files
            foreach (Scene scene in scenes)
            {
                string fileName = "3d-" + (i++) + ".fbx";
                scene.Save(RunExamples.GetOutputFilePath(fileName), FileFormat.FBX7400ASCII);
            }

{{< /highlight >}}

{{% alert color="primary" %}}

Tutti i formati di file 3D supportati sono elencati nella pagina [Panoramica del prodotto](/3d/it/net/product-overview/).

{{% /alert %}}
