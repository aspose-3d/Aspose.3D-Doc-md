---
title: Sparen Sie eine 3D-Szene in PDF in C#
linktitle: Sparen Sie eine 3D-Szene in der PDF
type: docs
weight: 60
url: /de/net/save-a-3d-scene-in-the-pdf/
description: Die Scene-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können eine 3D-Szene erstellen, indem sie Kamera, Licht, Polygone und verschiedene andere Entitäten hinzufügen. Sie können jetzt auch eine 3D-Szene im PDF-Dateiformat speichern.
---
##  **Übersicht**

Dieser Artikel erklärt, wie Sie 3D-Datei in PDF-Format konvertieren können, indem Sie C# .NET 3D Datei manipulation und-konvertierung API verwenden. Zuerst müssen Sie [Laden Sie die 3D-Datei in das Scene-Objekt](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) und dann im PDF-Format speichern. Es deckt ein breites Themen spektrum ab, z.

- 3D zu PDF in C# umrechnen
- FBX zu PDF in C# umrechnen
- STL zu PDF in C# umrechnen
- U3D zu PDF in C# umrechnen
- OBJ zu PDF in C# umrechnen

{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können eine 3D-Szene erstellen, indem sie Kamera, Licht, Polygone und verschiedene andere Entitäten hinzufügen. Sie können jetzt auch eine 3D-Szene im PDF-Dateiformat speichern.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET schreibt direkt die Informationen über API und Versions nummer in Ausgabe dokumenten. Zum Beispiel beim Rendern einer Zeichnung nach PDF, Aspose.3D for .NET füllt `Application` Feld mit Wert 'Aspose. Feld 3D' und `PDF Producer` mit Wert, e.g 'Aspose.3D 17,9'.

Bitte beachten Sie, dass Sie Aspose.3D for .NET API nicht anweisen können, diese Informationen aus Ausgabe dokumenten zu ändern oder zu entfernen.

{{% /alert %}} 
##  **Erstellen Sie einen 3D PDF mit einem Zylinder und rendern Sie ihn im schattierten Illustration modus mit einer optimierten Beleuchtung von CAD**
Die Save-Methode der `Scene`-Klasse ermöglicht es, eine 3D-Szene im PDF-Format zu speichern. Entwickler können jede von 3D unterstützte Datei laden oder eine neue 3D-Szene erstellen. Sie können eine 3D-Szene im PDF-Format speichern, wie in diesem C#-Code beispiel gezeigt:

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
