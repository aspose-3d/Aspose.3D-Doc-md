---
title: "Ajout d'une transformation au nœud"
type: docs
weight: 10
url: "/fr/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D pour Node.js via l'API Java prend en charge la rotation des objets dans l'espace 3D. Il existe trois façons de définir la rotation d'un objet dans l'espace 3D : les angles d'Euler, les quaternions et une matrice personnalisée, tous pris en charge par la classe Transform."
---

{{% alert color="primary" %}}

Aspose.3D pour Node.js via l’API Java prend en charge la rotation des objets dans l’espace 3D. Il existe trois façons de définir la rotation d’un objet dans l’espace 3D : les angles d’Euler, les quaternions et la matrice personnalisée, toutes prises en charge par la classe `Transform`.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) sont le plus couramment utilisés dans les scénarios 3D, nous avons fourni une classe `Transform` pour y accéder dans Aspose.3D. Les transformations affines incluent :

- Translation
- Scaling
- Rotation
- Shear mapping
- Squeeze mapping

## **Rotation par angles d’Euler**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l’objet scène
var scene = new aspose.threed.Scene();

// Initialiser le cylindre
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Créer ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Angles d’Euler
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Définir la translation
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Sauvegarder
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Matrice de transformation personnalisée**
Nous pouvons également utiliser Matrix directement :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l’objet scène
var scene = new aspose.threed.Scene();

// Initialiser le cylindre
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Créer ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Définir la matrice de translation personnalisée
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Sauvegarder
scene.save("TransformationToNode.obj");

{{< /highlight >}}