---
title: "Material zu 3D-Entitäten hinzufügen"
type: docs
weight: 60
url: "/de/nodejs-java/add-material-to-3d-entities/"
description: "PBR spielt eine Schlüsselrolle für die Visualisierung von Spiele-Engines, mit seiner effizienten und realistischen Darstellung von Interaktionen zwischen Licht und Oberfläche durch Abmilderung der Helligkeit und Streuung des reflektierten Lichts. Entwickler können die Aspose.3D API verwenden, um PBR-Materialien auf 3D-Objekte in einer Szene anzuwenden. Dieses Codebeispiel demonstriert, wie ein Box-Objekt erstellt und dann das PBR-Material angewendet wird."
---

{{% alert color="primary" %}}

PBR spielt eine Schlüsselrolle für die Visualisierungen der Spiele-Engine, mit seiner effizienten und realistischen Darstellung von Wechselwirkungen zwischen Licht und Oberfläche durch Abschwächung der Helligkeit und Streuung des reflektierten Lichts. Entwickler können die Aspose.3D API verwenden, um PBR-Materialien auf 3D-Objekte in einer Szene anzuwenden. Dieses Codebeispiel demonstriert, wie ein Box-Objekt erstellt und dann das PBR-Material angewendet wird.

{{% /alert %}}

## **Physically Based Rendering (PBR)-Material auf einen Kasten anwenden**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// initialisiere eine Szene
var scene = new aspose.threed.Scene();

// initialisiere PBR-Materialobjekt
var mat = new aspose.threed.PbrMaterial();

// ein fast metallisches Material
mat.setMetallicFactor(0.9);

// die Materialoberfläche ist sehr rau
mat.setRoughnessFactor(0.9);

// erstelle einen Kasten, auf den das Material angewendet wird
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// speichere 3D-Szene im USDZ-Format
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}