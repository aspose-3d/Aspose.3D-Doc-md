---
title: Hinzufügen einer Asset-Information zur Szene
type: docs
weight: 10
url: /de/net/add-an-asset-information-to-scene
description: Metadaten sind strukturierte Informationen, die das Abrufen, Verwenden oder Verwalten einer Informations ressource beschreiben, erklären, lokalisieren oder erleichtern. Aspose.3D for .NET API ermöglicht es Entwicklern, Metadaten für die Szene zu definieren.
---
##  **Hinzufügen einer Asset-Information zur 3D-Szene**
Metadaten sind strukturierte Informationen, die das Abrufen, Verwenden oder Verwalten einer Informations ressource beschreiben, erklären, lokalisieren oder erleichtern. Aspose.3D for .NET API ermöglicht es Entwicklern, Metadaten für die Szene zu definieren.
###  **Definieren Sie eine Metadaten für die Szene**
3D Shows erzeugen riesige Mengen an Metadaten und Bild informationen. Metadaten sind ein Aktiv posten und Teil der Show.

1. Initial isieren Sie eine 3D-Szene mit der [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse.
1. Legen Sie den Namen der Anwendung/des Werkzeugs fest.
1. Legen Sie den Namen des Anwendungs-/Werkzeug herstellers fest.
1. Maßeinheit einstellen.
1. Maßeinheit Skalierung faktor festlegen.
1. Speichern Sie die 3D-Szene im unterstützten Dateiformat.

In diesem Beispiel nehmen wir an, dass die Szene von einem CAD-Tool namens "Egypt" erstellt wurde und von "Manualdesk" entworfen wurde:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a 3D scene
Scene scene = new Scene();

// Set application/tool name
scene.AssetInfo.ApplicationName = "Egypt";

// Set application/tool vendor name
scene.AssetInfo.ApplicationVendor = "Manualdesk";

// We use ancient egyption measurement unit Pole
scene.AssetInfo.UnitName = "pole";

// One Pole equals to 60cm
scene.AssetInfo.UnitScaleFactor = 0.6;

// Save scene to 3D supported file formats
scene.Save("InformationToScene.fbx");

{{< /highlight >}}
