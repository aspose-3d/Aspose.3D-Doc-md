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

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Retourner le système de coordonnées dans les formats 3D**
Aspose.3D for Python via .NET API permet aux utilisateurs de retourner le système de coordonnées dans les formats OBJ, 3DS, STL et U3D.

{{% alert color="primary" %}} 

Pour importer un fichier 3ds et l'enregistrer au format OBJ, la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) est utilisée dans le code.

{{% /alert %}} 

Dans cet exemple, nous avons inversé le système de coordonnées lors de l'importation du fichier 3ds et l'avons enregistré au format OBJ sans matériaux.
