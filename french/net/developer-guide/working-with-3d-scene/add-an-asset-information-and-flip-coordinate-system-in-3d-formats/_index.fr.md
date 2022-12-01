---
title: Ajouter un système d'informations sur les actifs et de coordonnées Flip dans les formats 3D
type: docs
weight: 10
url: /fr/net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for .NET API permet aux développeurs de définir une métadonnée pour la scène.
---
## **Ajouter une information sur les actifs à 3D Scène**
Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for .NET API permet aux développeurs de définir une métadonnée pour la scène.
### **Définir une métadonnée pour la scène**
Les émissions 3D produisent des quantités massives de métadonnées et d'informations sur l'image. Les métadonnées sont un atout et font partie du spectacle.

1. Initialisez une scène 3D en utilisant la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene).
1. Définir le nom de l'application/outil.
1. Définir le nom du fournisseur d'application/outil.
1. Définir l'unité de mesure.
1. Définir le facteur d'échelle de l'unité de mesure.
1. Enregistrez 3D scène dans le format de fichier pris en charge.

Dans cet exemple, nous supposons que la scène est créée par un outil CAD appelé «Egypt» et qu'elle est conçue par «Manualdesk»:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-AssetInformation-InformationToScene-AddAssetInformationToScene.cs" >}}
## **Système de coordonnées Flip dans les formats 3D**
Aspose.3D for .NET API permet aux utilisateurs de basculer le système de coordonnées aux formats OBJ, 3DS, STL et U3D.

{{% alert color="primary" %}} 

Pour importer un fichier 3ds et l'enregistrer au format OBJ, la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) est utilisée dans le code.

{{% /alert %}} 

Dans cet exemple, nous avons inversé le système de coordonnées tout en important le fichier 3ds, et nous l'avons enregistré au format OBJ sans matériaux.
