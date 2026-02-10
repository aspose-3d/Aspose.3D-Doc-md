---
title: Asset-Informationen zum 3D-Dokument hinzufügen
type: docs
weight: 10
url: /de/java/add-asset-information-to-3d-document/
description: Metadaten sind strukturierte Informationen, die das Abrufen, Verwenden oder Verwalten einer Informations ressource beschreiben, erklären, lokalisieren oder erleichtern. Aspose.3D for Java API bietet Unterstützung für die Definition von Metadaten für die Szene.
---
##  **Asset-Informationen zum 3D-Dokument hinzufügen**
Metadaten sind strukturierte Informationen, die das Abrufen, Verwenden oder Verwalten einer Informations ressource beschreiben, erklären, lokalisieren oder erleichtern. Aspose.3D for Java API bietet Unterstützung für die Definition von Metadaten für die Szene.
###  **Definieren Sie eine Metadaten für die Szene**
3D Shows erzeugen riesige Mengen an Metadaten und Bild informationen. Metadaten sind ein Aktiv posten und Teil der Show.

1. Initial isieren Sie eine 3D-Szene mit der `Scene`-Klasse.
1. Legen Sie den Namen der Anwendung/des Werkzeugs fest.
1. Legen Sie den Namen des Anwendungs-/Werkzeug herstellers fest.
1. Maßeinheit einstellen.
1. Maßeinheit Skalierung faktor festlegen.
1. Speichern Sie die 3D-Szene im unterstützten Dateiformat.

In diesem Beispiel nehmen wir an, dass die Szene von einem CAD-Tool namens "Egypt" erstellt wurde und von "Manualdesk" entworfen wurde:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
