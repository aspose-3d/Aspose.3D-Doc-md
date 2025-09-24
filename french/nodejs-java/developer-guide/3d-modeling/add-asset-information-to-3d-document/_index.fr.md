---
title: Ajouter des informations sur les ressources au document 3D
type: docs
weight: 10
url: "/fr/nodejs-java/add-asset-information-to-3d-document/"
description: "Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D pour Node.js via Java API prend en charge la définition de métadonnées pour la scène."
---

## **Ajouter des informations sur les actifs à un document 3D**
Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l’utilisation ou la gestion d’une ressource d’information. Aspose.3D pour Node.js via Java API prend en charge la définition de métadonnées pour la scène.
### **Définir des métadonnées pour la scène**
Les productions 3D génèrent d’énormes quantités de métadonnées et d’informations sur les images. Les métadonnées sont un actif et font partie du spectacle.

1. Initialiser une scène 3D à l’aide de la classe `Scene`.
1. Définir le nom de l’application/de l’outil.
1. Définir le nom du fournisseur d’application/d’outil.
2. Définir l’unité de mesure.
3. Définir le facteur d’échelle de l’unité de mesure.
4. Enregistrer la scène 3D dans un format de fichier pris en charge.

Dans cet exemple, nous supposons que la scène est créée par un outil CAD appelé « Egypt » et qu’elle est conçue par « Manualdesk » :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser une scène 3D
var scene = new aspose.threed.Scene();

// Initialiser l’objet Box
var box=new aspose.threed.Box();

// Ajouter l’objet Box à la scène
scene.getRootNode().createChildNode(box);

// Définir le nom de l’application/de l’outil
scene.getAssetInfo().setApplicationName("Egypt");

// Définir le nom du fournisseur d’application/de l’outil
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// Nous utilisons l’unité de mesure égyptienne antique, le Pole
scene.getAssetInfo().setUnitName("pole");

// Un Pole équivaut à 60 cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}