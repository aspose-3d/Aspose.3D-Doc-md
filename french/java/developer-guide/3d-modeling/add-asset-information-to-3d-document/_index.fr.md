---
title: Ajouter des informations sur les actifs au document 3D
type: docs
weight: 10
url: /fr/java/add-asset-information-to-3d-document/
description: Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for Java API a le support pour définir les métadonnées de la scène.
---
##  **Ajouter des informations sur les actifs au document 3D**
Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for Java API a le support pour définir les métadonnées de la scène.
###  **Définir une métadonnée pour la scène**
3D montre produire des quantités massives de métadonnées et des informations d'image. Les métadonnées sont un atout et font partie du spectacle.

1. Initialisez une scène 3D en utilisant la classe `Scene`.
1. Définir le nom de l'application/outil.
1. Définir le nom du fournisseur d'application/outil.
1. Définir l'unité de mesure.
1. Définir le facteur d'échelle de l'unité de mesure.
1. Enregistrez la scène 3D dans le format de fichier pris en charge.

Dans cet exemple, nous supposons que la scène est créée par un outil CAD appelé «Egypt» et qu'elle est conçue par «Manualdesk»:

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
