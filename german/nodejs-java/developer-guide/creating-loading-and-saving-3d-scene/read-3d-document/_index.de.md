---
title: "Lese 3D-Dokument"
type: docs
weight: 30
url: "/de/nodejs-java/read-3d-document/"
description: "Aspose.3D für Node.js über Java API unterstützt das Lesen verschiedener Arten von 3D-Dokumenten."
---

## **Liste der unterstützten 3D-Formate (Import)**
Aspose.3D für Node.js über die Java API unterstützt das Lesen verschiedener Arten von 3D-Dokumenten. Die verfügbaren Konstruktoren der Klasse `Scene` helfen dabei und akzeptieren einen gültigen Dateipfad-String. Die unterstützten lesbaren Dateiformate sind wie folgt:

1. FBX 7.5 (ASCII, Binär)
1. FBX 7.4 (ASCII, Binär)
1. FBX 7.3 (ASCII, Binär)
1. FBX 7.2 (ASCII, Binär)
1. STL (ASCII, Binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binär)
1. X (ASCII, Binär)
1. Draco
1. 3MF
1. RVM (Text, Binär)
1. ASE

Die Konstruktoren der Klasse Scene erkennen das 3D-Dokumentformat intern.
## **3D-Dokument importieren**
Aspose.3D für die Java API unterstützt das Importieren verschiedener Arten von 3D-Dokumenten für Modifikations-, Additions- und Verarbeitungszwecke.
### **Eine 3D-Szene lesen: Programmierbeispiele**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisieren eines Klassenobjekts Scene
var scene = new aspose.threed.Scene();

// Laden eines vorhandenen 3D-Dokuments
scene.open( "document.obj");

{{< /highlight >}}