---
title: "Asset-Informationen zu 3D-Dokument hinzufügen"
type: docs
weight: 10
url: "/de/nodejs-java/add-asset-information-to-3d-document/"
description: Metadaten sind strukturierte Informationen, die einen Informationsbestand beschreiben, erklären, lokalisieren oder die Wiederverwendung oder Verwaltung erleichtern. Aspose.3D für Node.js über Java API unterstützt die Definition von Metadaten für die Szene.
---

## **Vermögensinformationen zu 3D-Dokument hinzufügen**
Metadaten sind strukturierte Informationen, die einen Informationsressourcen beschreiben, erklären, lokalisieren oder die Wiederverwendung oder Verwaltung erleichtern. Aspose.3D für Node.js via Java API unterstützt die Definition von Metadaten für die Szene.
### **Metadaten für die Szene definieren**
3D-Shows produzieren riesige Mengen an Metadaten und Bildinformationen. Metadaten sind ein Vermögenswert und Teil der Show.

1. Initialisieren Sie eine 3D-Szene mit der Klasse `Scene`.
1. Legen Sie den Anwendungs-/Toolnamen fest.
2. Legen Sie den Anwendungs-/Tool-Vendor-Namen fest.
3. Legen Sie die Maßeinheit fest.
4. Legen Sie den Maßeinheitsskalierungsfaktor fest.
5. Speichern Sie die 3D-Szene im unterstützten Dateiformat.

In diesem Beispiel wird davon ausgegangen, dass die Szene von einem CAD-Tool namens „Egypt“ erstellt wurde und von „Manualdesk“ entworfen wurde:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisieren Sie eine 3D-Szene
var scene = new aspose.threed.Scene();

// Initialisieren Sie das Box-Objekt
var box=new aspose.threed.Box();

// Fügen Sie das Box-Objekt zur Szene hinzu
scene.getRootNode().createChildNode(box);

// Legen Sie den Anwendungs-/Toolnamen fest
scene.getAssetInfo().setApplicationName("Egypt");

// Legen Sie den Anwendungs-/Tool-Vendor-Namen fest
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// Wir verwenden die altägyptische Maßeinheit Pole
scene.getAssetInfo().setUnitName("pole");

// Ein Pole entspricht 60 cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}