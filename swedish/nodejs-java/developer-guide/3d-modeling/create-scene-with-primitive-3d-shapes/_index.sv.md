---
title: "Skapa scen med primitiva 3D-former"
type: docs
weight: 20
url: "/sv/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: "Aspose.3D för Node.js via Java API har stöd för primitiva 3D-former. Alla parameterstyrda primitiva former kommer att konverteras till nät automatiskt vid sparande i alla stödda utdatafilformat."
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API har stöd för primitiva 3D-former. Alla parameteriserade primitiva former kommer att konverteras till mesh automatiskt vid sparande i något av de stödda utdatafilformaten.

{{% /alert %}} 
## **Skapa Scen från Primitiva 3D-former**
Modellering är en process av ren skapelse och Aspose.3D API stöder skapandet av en scen med primitiva 3D-former.
### **Programmerings Exempel**
Detta kodexempel skapar en scen med primitiva 3D-former och sparar i OBJ-filen.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera en 3D-scen
var scene = new aspose.threed.Scene();

// Skapa en Box-modell
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Skapa en Cylinder-modell
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Spara ritning i OBJ-formatet
scene.save("test.obj");


{{< /highlight >}}