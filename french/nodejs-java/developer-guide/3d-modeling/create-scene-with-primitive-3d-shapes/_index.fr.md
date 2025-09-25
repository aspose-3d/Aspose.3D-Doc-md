---
title: Créer une scène avec des formes 3D primitives
type: docs
weight: 20
url: "/fr/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: "Aspose.3D pour Node.js via l'API Java prend en charge les formes 3D primitives. Toutes les primitives paramétrées seront converties en maillage automatiquement lors de la sauvegarde dans n'importe quel format de fichier de sortie pris en charge."
---

{{% alert color="primary" %}} 

Aspose.3D pour Node.js via Java API prend en charge les formes 3D primitives. Toutes les primitives paramétrées seront converties en maillage lors de la sauvegarde dans n'importe quel format de fichier de sortie pris en charge.

{{% /alert %}} 
## **Construire une Scène à partir de Formes 3D Primitives**
La modélisation est le processus de pure création et l'API Aspose.3D prend en charge la création d'une scène avec des formes 3D primitives.
### **Exemple de Programmation**
Cet exemple de code crée une scène avec des formes 3D primitives et l'enregistre dans le fichier OBJ.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser une scène 3D
var scene = new aspose.threed.Scene();

// Créer un modèle Box
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Créer un modèle Cylinder
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Enregistrer le dessin dans le format OBJ
scene.save("test.obj");


{{< /highlight >}}