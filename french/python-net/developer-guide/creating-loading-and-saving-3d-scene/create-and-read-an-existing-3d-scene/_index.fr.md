---
title: Créer et lire une scène 3D existante
type: docs
weight: 10
url: /fr/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis les sauvegarde dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'ajout ou de traitement.
---
##  **Créez une scène 3D vide et enregistrez dans les formats de fichier 3D pris en charge**
Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis les sauvegarde dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'ajout ou de traitement.
###  **Création d'un document de scène 3D**
Veuillez suivre ces étapes pour créer un document de scène 3D à l'aide des API Aspose.3D:

1. Créez une instance de la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui représente un document de scène 3D.
1. Générez un document de scène 3D en appelant la méthode [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) de l'objet de classe Scene.
####  **Création d'un document de scène 3D: Programmation des exemples**


{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Lecture d'une scène 3D**
En utilisant Aspose.3D API, les développeurs peuvent charger tous les documents 3D pris en charge. Les constructeurs disponibles du**Scène**La classe permet de le faire et ils acceptent une chaîne de chemin de fichier valide. Les formats de fichiers lisibles pris en charge sont les suivants:

1. FBX 7.7 (ASCII, binaire)
1. FBX 7.6 (ASCII, Binaire)
1. FBX 7.5 (ASCII, binaire)
1. FBX 7.4 (ASCII, binaire)
1. FBX 7.3 (ASCII, binaire)
1. FBX 7.2 (ASCII, binaire)
1. STL (ASCII, binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binaire)
1. X (ASCII, binaire)
1. XYZ
1. Draco
1. 3MF
1. RVM (Texte, Binaire)
1. ASE
1. USDZ
1. USD

Les constructeurs de la classe `Scene` détectent le format de document 3D en interne.
###  **Lecture d'une scène 3D: Échantillons de programmation**
{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")


{{< /highlight >}}
