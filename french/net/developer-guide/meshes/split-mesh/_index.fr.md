---
title: Maille fendue
type: docs
weight: 100
url: /fr/net/split-mesh/
description: Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant Aspose.3D for .NET API.
---
##  **Divisez tous les mailles d'une scène par matériau**
Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum spécifie la politique de données utilisée dans l'algorithme de division de maillage, il prend en charge deux politiques, partage de données entre sous-maillages ou chaque sous-maillage a ses propres données (uniquement des données utilisées).

{{% /alert %}}

L'échantillon de code ci-dessous divise toutes les mailles d'une scène par matériau. Chaque sous-maillage partage les mêmes données directes et ne diffère que dans les indices.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
##  **Diviser un maillage en spécifiant le matériau**
Aspose.3D for .NET API permet aux développeurs de diviser un maillage en spécifiant manuellement le matériau. L'option de maillage fractionné crée des objets séparés et chaque sous maillage utilisera un seul matériau.
###  **Fendre la maille de la boîte**
Cette rubrique d'aide crée un maillage de la boîte pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer un maillage de cube 3D](/3d/fr/net/create-3d-mesh-and-scene/). En outre, une boîte est composée de 6 plans et chaque plan deviendra un sous-maillage. L'exemple de code ci-dessous divise un maillage primitif en spécifiant manuellement le matériau.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
