---
title: Exposer la Transformation Géométrique
type: docs
weight: 50
url: "/fr/nodejs-java/expose-geometric-transformation/"
description: "Aspose.3D pour Node.js via Java permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale en utilisant la méthode evaluateGlobalTransform."
---

# **Exposer la Transformation Géométrique**
Aspose.3D pour Node.js via Java permet d'exposer la transformation géométrique d'une scène 3D. Vous pouvez évaluer la transformation globale en utilisant la méthode `evaluateGlobalTransform`. Le code ci-dessous montre comment exposer la transformation géométrique.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l'objet scène
var scene = new aspose.threed.Scene();

// Initialiser le cylindre
var cylinder =new aspose.threed.Cylinder();

// Créer ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Obtenir la Translation Géométrique
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// La première Console.WriteLine affichera la matrice de transformation qui inclut la transformation géométrique
// tandis que la seconde ne le fera pas.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}