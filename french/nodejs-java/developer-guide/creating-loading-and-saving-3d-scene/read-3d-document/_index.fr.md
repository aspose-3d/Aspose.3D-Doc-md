---
title: Lire un document 3D
type: docs
weight: 30
url: "/fr/nodejs-java/read-3d-document/"
description: Aspose.3D pour Node.js via l’API Java prend en charge la lecture de divers types de documents 3D.
---

## **Liste des formats 3D pris en charge (importation)**
Aspose.3D pour Node.js via l'API Java prend en charge la lecture de divers types de documents 3D. Les constructeurs disponibles de la classe `Scene` permettent de le faire et ils acceptent une chaîne de chemin de fichier valide. Les formats de fichiers lisibles pris en charge sont les suivants :

1. FBX 7.5 (ASCII, Binaire)
1. FBX 7.4 (ASCII, Binaire)
1. FBX 7.3 (ASCII, Binaire)
1. FBX 7.2 (ASCII, Binaire)
1. STL (ASCII, Binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binaire)
1. X (ASCII, Binaire)
1. Draco
1. 3MF
1. RVM (Texte, Binaire)
1. ASE

Les constructeurs de la classe Scene détectent le format du document 3D en interne.
## **Importer un document 3D**
Aspose.3D pour l'API Java prend en charge l'importation de divers types de documents 3D à des fins de modification, d'ajout et de traitement.
### **Lecture d'une scène 3D : Exemples de programmation**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser un objet de classe Scene
var scene = new aspose.threed.Scene();

// Charger un document 3D existant
scene.open( "document.obj");

{{< /highlight >}}