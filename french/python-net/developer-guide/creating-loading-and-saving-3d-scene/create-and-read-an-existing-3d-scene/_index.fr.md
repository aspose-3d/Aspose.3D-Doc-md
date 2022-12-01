---
title: Créer et lire une scène 3D existante
type: docs
weight: 10
url: /fr/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis enregistrez-les dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'addition ou de traitement.
---
## **Créer une scène 3D vide et enregistrer dans les formats de fichier 3D pris en charge**
Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis enregistrez-les dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'addition ou de traitement.
### **Création d'un document de scène 3D**
Veuillez suivre ces étapes pour créer un document Scène 3D en utilisant les API Aspose.3D:

1. Créez une instance de la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui représente un document de scène 3D.
1. Générer un document Scène 3D en appelant la méthode [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) de l'objet de classe Scène.
#### **Création d'un document scène 3D: Échantillons de programmation**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
## **Lecture d'une scène 3D**
En utilisant Aspose.3D API, les développeurs peuvent charger tous les documents 3D pris en charge. Les constructeurs disponibles de la**Scène**La classe permet de le faire et ils acceptent une chaîne de chemin de fichier valide. Les formats de fichiers lisibles pris en charge sont les suivants:

1. FBX 7.7 (ASCII, Binaire)
1. FBX 7.6 (ASCII, Binaire)
1. FBX 7.5 (ASCII, binaire)
1. FBX 7.4 (ASCII, Binaire)
1. FBX 7.3 (ASCII, Binaire)
1. FBX 7.2 (ASCII, binaire)
1. STL (ASCII, Binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binaire)
1. X (ASCII, binaire)
1. XYZ
1. Draco
1. 3MF
1. RVM (Texte, Binaire)
1. ASE
1. USDZ
1. USD

Les constructeurs de la classe `Scene` détectent le format de document 3D en interne.
### **Lecture d'une scène 3D: Échantillons de programmation**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
