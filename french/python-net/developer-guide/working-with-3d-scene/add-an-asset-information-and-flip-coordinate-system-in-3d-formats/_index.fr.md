---
title: Ajouter un système d'informations sur les actifs et de coordonnées Flip dans les formats 3D
type: docs
weight: 10
url: /fr/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for Python via .NET API permet aux développeurs de définir des métadonnées pour la scène.
---
##  **Ajouter une information d'actif à la scène 3D**
Les métadonnées sont des informations structurées qui décrivent, expliquent, localisent ou facilitent la récupération, l'utilisation ou la gestion d'une ressource d'information. Aspose.3D for Python via .NET API permet aux développeurs de définir des métadonnées pour la scène.
###  **Définir une métadonnée pour la scène**
3D montre produire des quantités massives de métadonnées et des informations d'image. Les métadonnées sont un atout et font partie du spectacle.

1. Initialisez une scène 3D en utilisant la classe `Scene`.
1. Définir le nom de l'application/outil.
1. Définir le nom du fournisseur d'application/outil.
1. Définir l'unité de mesure.
1. Définir le facteur d'échelle de l'unité de mesure.
1. Enregistrez la scène 3D dans le format de fichier pris en charge.

Dans cet exemple, nous supposons que la scène est créée par un outil CAD appelé «Egypt» et qu'elle est conçue par «Manualdesk»:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
##  **Retourner le système de coordonnées dans les formats 3D**
Aspose.3D for Python via .NET API permet aux utilisateurs de retourner le système de coordonnées dans les formats OBJ, 3DS, STL et U3D.

{{% alert color="primary" %}} 

Pour importer un fichier 3ds et l'enregistrer au format OBJ, la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) est utilisée dans le code.

{{% /alert %}} 

Dans cet exemple, nous avons inversé le système de coordonnées lors de l'importation du fichier 3ds et l'avons enregistré au format OBJ sans matériaux.
