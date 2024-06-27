---
title: Générer des données normales pour tous les maillages dans un fichier 3D
type: docs
weight: 70
url: /fr/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: En utilisant Aspose.3D for Python via .NET, les développeurs peuvent générer des données normales pour tous les maillages dans n'importe quel modèle 3D (sans les données normales).
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), les développeurs peuvent générer des données normales pour tous les maillages dans n'importe quel modèle 3D (sans les données normales).

{{% /alert %}}
##  **Générer des données normales pour tous les maillages dans un fichier 3DS**
La méthode `generate_normal` exposée par la classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) peut être utilisée pour générer des données normales pour tous les maillages d'un fichier 3DS. Si l'élément `VertexElementSmoothingGroup` a été défini dans le maillage, les données normales générées seront lissées par le `VertexElementSmoothingGroup`.
###  **Échantillon de programmation**
Cet exemple de code charge un fichier 3DS, visite tous les nœuds et crée des données normales pour tous les maillages.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
