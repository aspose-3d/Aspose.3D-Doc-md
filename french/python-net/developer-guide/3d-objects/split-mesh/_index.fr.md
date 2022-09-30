---
title: Maille fendue
type: docs
weight: 100
url: /fr/python-net/split-mesh/
description: Les développeurs peuvent exiger de diviser toutes les mailles d'une scène en plusieurs sous-mailles par matériau. La méthode SplitMesh ne divisera pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant Aspose.3D pour Python via .NET API.
---
## **Divisez tous les mailles d'une scène par matériau**
Les développeurs peuvent exiger de diviser toutes les mailles d'une scène en plusieurs sous-mailles par matériau. La méthode `split_mesh` ne divisera pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant[Aspose.3D pour Python via .NET](https://products.aspose.com/3d/python-net/)API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum spécifie la politique de données utilisée dans l'algorithme de fractionnement de maillage, il prend en charge deux politiques, partage des données entre des sous-maillages ou chaque sous-maillage a ses propres données (données utilisées uniquement).

{{% /alert %}}

L'échantillon de code ci-dessous divise toutes les mailles d'une scène par matériau. Chaque sous-maillage partage les mêmes données directes et ne diffère que dans les indices.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
## **Diviser un maillage en spécifiant le matériau**
Aspose.3D pour Python via .NET API permet aux développeurs de diviser un maillage en spécifiant manuellement le matériau. L'option de maillage divisé crée des objets séparés et chaque sous-maillage n'utilisera qu'un seul matériau.
### **Fendre la maille de la boîte**
Ce sujet d'aide crée un maillage de la boîte pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme raconté dans ce sujet d'aide:[Créer un maillage Cube 3D](/3d/fr/python-net/create-3d-mesh-and-scene/). De plus, une boîte est composée de 6 plans et chaque plan deviendra un sous-maillage. L'échantillon de code ci-dessous divise un maillage primitif en spécifiant manuellement le matériau.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
