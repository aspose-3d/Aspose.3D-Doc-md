---
title: "Lägg till material till 3D-entiteter"
type: docs
weight: 60
url: "/sv/nodejs-java/add-material-to-3d-entities/"
description: "PBR spelar en nyckelroll för spelmotorns visuella presentation, med sin effektiva och realistiska återgivning av interaktioner mellan ljus och yta via dämpning av ljusstyrkan och spridning av reflekterat ljus. Utvecklare kan använda Aspose.3D API för att tillämpa PBR-material på 3D-objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan tillämpar PBR-materialet."
---

{{% alert color="primary" %}}

PBR spelar en nyckelroll för spelmotorns visuella presentation, med sin effektiva och realistiska återgivning av interaktioner mellan ljus och yta via dämpning av ljusstyrkan och spridning av reflekterat ljus. Utvecklare kan använda Aspose.3D API för att applicera PBR-material till 3D-objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan applicerar PBR-materialet.

{{% /alert %}}

## **Applicera Physically Based Rendering (PBR) Material till en Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// initialisera en scen
var scene = new aspose.threed.Scene();

// initialisera PBR materialobjekt
var mat = new aspose.threed.PbrMaterial();

// ett nästan metalliskt material
mat.setMetallicFactor(0.9);

// materialytan är mycket grov
mat.setRoughnessFactor(0.9);

// skapa en box till vilken materialet ska appliceras
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// spara 3d-scen i USDZ-format
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}