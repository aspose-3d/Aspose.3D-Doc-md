---
title: So führen Sie Aspose.3D in Blazor aus
type: docs
weight: 138
url: /de/net/how-to-run-aspose-3d-in-blazor/
description: Erfahren Sie, wie Sie Aspose.3D in Blazor ausführen.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Übersicht

Blazor ist ein von Microsoft entwickeltes Web anwendungs framework, mit dem clients eitige Web anwendungen mit C# und .NET geschrieben werden können. Blazor zeichnet sich durch die Verwendung der WebAssembly-Technologie aus, mit der im Browser ausgeführte Anwendungen hoch leistungs fähigen nativen Code verwenden können. Blazor verwendet eine komponenten isierte Architektur, mit der Entwickler die Benutzer oberfläche in unabhängige Komponenten aufteilen können, wodurch die Wieder verwendbar keit und Wartbarkeit von Code erreicht wird. Blazor unterstützt die plattform übergreifende Entwicklung und kann auf einer Vielzahl moderner Browser und Geräte ausgeführt werden, einschl ießlich Desktop-, Mobilgeräte und eingebettete Geräte.

In general, Blazor provides a modern way to build web applications, enabling developers to build high-performance, interactive, and maintainable web applications using C# and .NET technologies in the browser.

## Erste Blazor-Bewerbung mit Aspose.3D

In diesem Beispiel haben wir eine einfache Blazor-Server anwendung erstellt, eine 3D-Datei erstellt, einen Screenshot des Datei inhalts erstellt und auf einer Webseite angezeigt. Während des Projekt erstellung prozesses können wir es entsprechend unseren Anforderungen konfigurieren, z. B. die Option "Enable Docker", damit die Blazor-Anwendung in Docker erstellt und ausgeführt werden kann.

### Erstellen Sie die erste Blazor-Anwendung

Let's use the VS2022 tool as an example to create the first blazor application with Aspose.3D, follow the steps below:
1. Wählen Sie Datei-> Neu-> Projekt und filtern Sie mit dem Blazer-Schlüssel wort, um die entsprechende Projekt vorlage auszuwählen.
<br>
<img src="1.png" width=80% />
1. Setzen Sie den Projektnamen auf "Blazor Test" und wählen Sie den Pfad aus.
<br>
<img src="2.png" width=80% />
1. Konfigurieren Sie die Bibliotheken und andere Optionen, die im Projekt verwendet werden. Klicken Sie abschließend auf die Schaltfläche "Erstellen", um Ihr erstes Blazer-Projekt zu generieren.
<br>
<img src="3.png" width=80% />
1. Nachdem Sie das Projekt eingegeben haben, klicken Sie auf "Abhängigkeiten" unter dem Projekt und wählen Sie "NuGet Pakete verwalten...", um die Aspose.3D Bibliothek hinzuzufügen.
<br>
<img src="4.png" width=80% />
1. Geben Sie Schlüssel wörter für die Filterung ein und installieren Sie die neueste Aspose.3D Bibliothek.
<br>
<img src="5.png" width=80% />
1. Doppelklicken Sie auf die Datei "Index. rasierer", um die gewünschte Bibliothek zu bearbeiten und zu importieren. Fügen Sie einige Daten und Bilder hinzu.
<br>
<img src="5.png" width=80% />
1. Kompilieren und führen Sie das Projekt aus, und Sie erhalten die folgenden Ergebnisse.
<br>
<img src="7.png" width=80% />

### Beispielcode in der ersten Blazor-Anwendung

Der folgende Beispielcode ist in der Datei Index. rasierer enthalten:
```
@page "/"
@using Aspose.ThreeD;
@using Aspose.ThreeD.Entities;
@using Aspose.ThreeD.Utilities;

<PageTitle>Index</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<SurveyPrompt Title="How is Blazor working for you?" />

<img src="@imageUrl" />

@code
{
    private string imageUrl="https://docs.aspose.com/3d/net/working-with-cylinder/working-with-cylinder_1.png";

    public Index()
    {
        CreateFile();
    }

    private void CreateFile()
    {
        // Create a scene
        Scene scene = new Scene();

        // Initialize cylinder
        var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

        // Set OffsetTop
        cylinder1.OffsetTop = new Vector3(5, 3, 0);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

        // Intialze second cylinder without customized OffsetTop
        var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder2);

        // Save
        scene.Save("CustomizedOffsetTopCylinder.obj");
    }
}

```