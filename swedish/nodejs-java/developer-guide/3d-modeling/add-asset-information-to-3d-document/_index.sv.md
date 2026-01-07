---
title: "Lägg till tillgångsinformation till 3D-dokument"
type: docs
weight: 10
url: "/sv/nodejs-java/add-asset-information-to-3d-document/"
description: Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D för Node.js via Java API har stöd för att definiera Metadata för scenen.
---

## **Lägg till tillgångsinformation till 3D-dokument**
Metadatan är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D för Node.js via Java API har stöd för att definiera metadata för scenen.
### **Definiera en metadata för scenen**
3D-produktioner producerar stora mängder metadata och bildinformation. Metadata är en tillgång och en del av produktionen.

1. Initialisera en 3D-scen med `Scene`-klassen.
1. Ange applikations-/verktygsnamn.
1. Ange applikations-/verktygsleverantörsnamn.
1. Ange måttenhet.
1. Ange måttenhetsskalningsfaktor.
1. Spara 3D-scenen i det stödda filformatet.

I det här exemplet antar vi att scenen är skapad av ett CAD-verktyg som heter "Egypten" och den är designad av "Manualdesk":

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera en 3D-scen
var scene = new aspose.threed.Scene();

// Initialisera Box-objektet
var box=new aspose.threed.Box();

// Lägg till Box-objektet till scenen
scene.getRootNode().createChildNode(box);

// Ange applikations-/verktygsnamn
scene.getAssetInfo().setApplicationName("Egypten");

// Ange applikations-/verktygsleverantörsnamn
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// Vi använder den forntida egyptiska måttenheten Pole
scene.getAssetInfo().setUnitName("pole");

// En Pole motsvarar 60 cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}