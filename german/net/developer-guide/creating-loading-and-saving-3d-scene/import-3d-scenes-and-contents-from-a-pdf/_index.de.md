---
title: Importieren Sie 3D Szenen und Inhalte aus einem PDF in C#
linktitle: Importieren Sie 3D Szenen und Inhalte aus einem PDF
type: docs
weight: 50
url: /de/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Die Scene-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können 3D Szenen und Inhalte aus einer PDF-Datei extrahieren.
---
{{% alert color="primary" %}}

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können 3D Szenen und Inhalte aus einer PDF-Datei extrahieren.

{{% /alert %}}
##  **Offene Szene aus einem Passwort geschützt PDF**
Die `Open`-Methode der `Scene`-Klasse erlaubt es, die 3D-Szene aus einer Eingabe-PDF-Datei zu laden. Entwickler können auch ein Passwort für die geschützten PDFs mit der [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions)-Klasse anwenden, wie in diesem C#-Code beispiel gezeigt:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a new scene
Scene scene = new Scene();
// Use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() { Password = Encoding.UTF8.GetBytes("password") };
// Open scene
scene.Open("House_Design.pdf", opt);

{{< /highlight >}}
##  **Extrahieren Sie alle Roh-3D-Inhalte aus einem PDF**
Die Extract-Methode der [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)-Klasse ermöglicht es, 3D-Inhalte aus einer PDF-Datei zu extrahieren. Entwickler können die Inhalte durchgehen und sie in den separaten Dateien speichern, wie in diesem Beispiel für C#-Code gezeigt:

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
##  **Extrahieren Sie alle 3D-Szenen und speichern Sie sie in unterstützten 3D-Formaten**
Die `ExtractScene`-Methode der `PdfFormat`-Klasse ermöglicht es, 3D-Szenen aus einer PDF-Datei zu extrahieren. Entwickler können die Szenen durchgehen und sie in den unterstützten 3D-Dateiformaten speichern, wie in diesem C#-Code beispiel gezeigt:

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

Alle unterstützten 3D-Dateiformate sind auf der [Produkt übersicht](/3d/de/net/product-overview/)-Seite aufgeführt.

{{% /alert %}}
