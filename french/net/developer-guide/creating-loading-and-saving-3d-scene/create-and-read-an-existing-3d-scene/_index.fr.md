---
title: Créer et lire une scène 3D existante
type: docs
weight: 10
url: /fr/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis les sauvegarde dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'ajout ou de traitement.
---
##  **Aperçu**
L'article explique les sujets suivants en utilisant la bibliothèque de manipulation des formats de fichiers C# 3D.
- Créer une scène vide 3D dans C# à partir de zéro
- Lire ou charger la scène 3D existante dans C#
- Enregistrez la scène 3D dans les formats 3D pris en charge à l'aide de C#
- Travailler avec 3D Propriétés de la scène dans C#

##  **Créez une scène 3D vide et enregistrez dans les formats de fichier 3D pris en charge**
Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis les sauvegarde dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'ajout ou de traitement.

###  **Création d'un document de scène 3D**
Veuillez suivre ces étapes dans C# pour créer un document scène 3D en utilisant les API Aspose.3D:

1. Créez une instance de la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui représente un document de scène 3D.
1. Générez un document de scène 3D en appelant la méthode [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) de l'objet de classe Scene.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

##  **Lecture d'une scène 3D**
En utilisant Aspose.3D API, les développeurs peuvent charger tous les documents 3D pris en charge. Les constructeurs disponibles de la classe `Scene` le permettent et ils acceptent une chaîne de chemin de fichier valide. Les formats de fichiers lisibles pris en charge sont les suivants:

1. FBX 7.5 (ASCII, binaire)
1. FBX 7.4 (ASCII, binaire)
1. FBX 7.3 (ASCII, binaire)
1. FBX 7.2 (ASCII, binaire)
1. FBX 6.1 (ASCII, binaire)
1. STL (ASCII, binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, binaire)
1. Maya (ASCII, binaire)
1. OpenUSD (USD, USDZ)
1. Mixeur
1. DXF
1. PLY (ASCII, binaire)
1. X (ASCII, binaire)
1. Draco
1. 3MF
1. RVM (Texte, Binaire)
1. ASE

Les constructeurs de la classe `Scene` détectent le format de document 3D en interne.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

##  **Travailler avec 3D Propriétés de scène**
Aspose.3D API vous permet de lire les propriétés de scène 3D en utilisant les nœuds enfants de la scène. L'exemple de code C# suivant illustre l'utilisation de cette fonctionnalité.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
