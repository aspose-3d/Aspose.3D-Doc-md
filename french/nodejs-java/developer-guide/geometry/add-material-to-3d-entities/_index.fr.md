---
title: Ajouter un matériau aux entités 3D
type: docs
weight: 60
url: "/fr/nodejs-java/add-material-to-3d-entities/"
description: "PBR joue un rôle clé pour les visuels du moteur de jeu, avec son rendu efficace et réaliste des interactions entre la lumière et la surface via l'atténuation de la luminosité et la diffusion de la lumière réfléchie. Les développeurs peuvent utiliser l'API Aspose.3D pour appliquer un matériau PBR aux objets 3D dans une scène. Cet exemple de code montre comment créer un objet Box, puis appliquer le matériau PBR."
---

{{% alert color="primary" %}}

PBR joue un rôle clé pour les visuels du moteur de jeu, avec son rendu efficace et réaliste des interactions entre la lumière et la surface via l'atténuation de la luminosité et la diffusion de la lumière réfléchie. Les développeurs peuvent utiliser l'API Aspose.3D pour appliquer un matériau PBR aux objets 3D dans une scène. Cet exemple de code montre comment créer un objet Box, puis appliquer le matériau PBR.

{{% /alert %}}

## **Appliquer un matériau de rendu basé sur la physique (PBR) à un Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// initialiser une scène
var scene = new aspose.threed.Scene();

// initialiser l'objet de matériau PBR
var mat = new aspose.threed.PbrMaterial();

// un matériau presque métallique
mat.setMetallicFactor(0.9);

// la surface du matériau est très rugueuse
mat.setRoughnessFactor(0.9);

// créer un box auquel le matériau sera appliqué
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// enregistrer la scène 3D au format USDZ
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}