---
title: Maille fendue
type: docs
weight: 100
url: /fr/python-net/split-mesh/
description: Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant Aspose.3D for Python via .NET API.
---
##  **Divisez tous les mailles d'une scène par matériau**
Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode `split_mesh` ne divisera pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum spécifie la politique de données utilisée dans l'algorithme de division de maillage, il prend en charge deux politiques, partage de données entre sous-maillages ou chaque sous-maillage a ses propres données (uniquement des données utilisées).

{{% /alert %}}

L'échantillon de code ci-dessous divise toutes les mailles d'une scène par matériau. Chaque sous-maillage partage les mêmes données directes et ne diffère que dans les indices.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
##  **Diviser un maillage en spécifiant le matériau**
Aspose.3D for Python via .NET API permet aux développeurs de diviser un maillage en spécifiant manuellement le matériau. L'option de maillage fractionné crée des objets séparés et chaque sous maillage utilisera un seul matériau.
###  **Fendre la maille de la boîte**
Cette rubrique d'aide crée un maillage de la boîte pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer un maillage de cube 3D](/3d/fr/python-net/create-3d-mesh-and-scene/). En outre, une boîte est composée de 6 plans et chaque plan deviendra un sous-maillage. L'exemple de code ci-dessous divise un maillage primitif en spécifiant manuellement le matériau.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
