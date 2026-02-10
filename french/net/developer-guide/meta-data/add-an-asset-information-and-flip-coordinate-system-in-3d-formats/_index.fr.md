---
title: Ajouter des informations d'actif à la scène
type: docs
weight: 10
url: /fr/net/add-an-asset-information-to-scene
description: Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for .NET API permet aux développeurs de définir des métadonnées pour la scène.
---
##  **Ajouter une information d'actif à la scène 3D**
Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for .NET API permet aux développeurs de définir des métadonnées pour la scène.
###  **Définir une métadonnée pour la scène**
3D montre produire des quantités massives de métadonnées et des informations d'image. Les métadonnées sont un atout et font partie du spectacle.

1. Initialisez une scène 3D en utilisant la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene).
1. Définir le nom de l'application/outil.
1. Définir le nom du fournisseur d'application/outil.
1. Définir l'unité de mesure.
1. Définir le facteur d'échelle de l'unité de mesure.
1. Enregistrez la scène 3D dans le format de fichier pris en charge.

Dans cet exemple, nous supposons que la scène est créée par un outil CAD appelé «Egypt» et qu'elle est conçue par «Manualdesk»:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a 3D scene
Scene scene = new Scene();

// Set application/tool name
scene.AssetInfo.ApplicationName = "Egypt";

// Set application/tool vendor name
scene.AssetInfo.ApplicationVendor = "Manualdesk";

// We use ancient egyption measurement unit Pole
scene.AssetInfo.UnitName = "pole";

// One Pole equals to 60cm
scene.AssetInfo.UnitScaleFactor = 0.6;

// Save scene to 3D supported file formats
scene.Save("InformationToScene.fbx");

{{< /highlight >}}
