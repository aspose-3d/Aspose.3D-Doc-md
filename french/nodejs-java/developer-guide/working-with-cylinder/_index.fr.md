---
title: Travailler avec le cylindre
type: docs
weight: 100
url: /fr/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java permet de personnaliser Offset Top d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la méthode setOffsetTop() de la classe Cylinder.
---
#  **Personnaliser le haut offset**
Aspose.3D for Node.js via Java permet de personnaliser Offset Top d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la méthode `setOffsetTop()` de la classe `Cylinder`. L'extrait de code suivant montre comment personnaliser Offset Top:



{{< highlight "java" >}}

// Create a scene
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder1 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Set OffsetTop
cylinder1.setOffsetTop(new aspose.threed.Vector3(5, 3, 0));

// Create ChildNode
var node1=scene.getRootNode().createChildNode(cylinder1);
node1.getTransform().setTranslation(new aspose.threed.Vector3(10, 0, 0));

// Initialize second cylinder without customized OffsetTop
var cylinder2 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
scene.getRootNode().createChildNode(cylinder2);

// Save
scene.save("CustomizedOffsetTopCylinder.obj");

{{< /highlight >}}

! [Tout le monde: image_alt_text](working-with-cylinder_1.png)

Celui de gauche a OffsetTop réglé sur (5, 3, 0), il est facile de voir que la casquette supérieure a bougé et que tout le torse est également affecté.
#  **Personnaliser ShearBottom**
Aspose.3D for Node.js via Java permet de personnaliser le fond de cisaillement d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété `setShearBottom()` de la classe `Cylinder`. L'extrait de code suivant montre comment personnaliser Shear Bottom:

{{< highlight "java" >}}

// Create a scene
var scene = new aspose.threed.Scene();

// Create cylinder 1
var cylinder1 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Customized shear bottom for cylinder 1
cylinder1.setShearBottom(new aspose.threed.Vector2(0, 0.83));

// Add cylinder 1 to the scene
var node1=scene.getRootNode().createChildNode(cylinder1);
node1.getTransform().setTranslation(new aspose.threed.Vector3(10, 0, 0));

// Create cylinder 2
var cylinder2 =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Add cylinder to without a ShearBottom to the scene
scene.getRootNode().createChildNode(cylinder2);

// Save scene
scene.save("CustomizedShearBottomCylinder.obj");

{{< /highlight >}}

! [Tout le monde: image_alt_text](working-with-cylinder_2.png)

Le cylindre gauche a ShearBottom à (0, 0,83) tandis que celui de droite est un cylindre ordinal.
#  **Créer un ventilateur-cylindre**
Aspose.3D for Node.js via Java permet de créer un cylindre de ventilateur. Afin d'utiliser cette fonctionnalité, vous pouvez `setGenerateFanCylinder()` de la classe `Cylinder` à `true`. L'extrait de code suivant montre comment utiliser cette fonctionnalité:

{{< highlight "java" >}}

// Create a scene
var scene = new aspose.threed.Scene();

// Create a cylinder
var fan  =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Set GenerateGanCylinder to true
fan.setGenerateFanCylinder(true);

// Set ThetaLength
fan.setThetaLength(aspose.threed.MathUtils.toRadian(270.0));

// Create ChildNode
var node1=scene.getRootNode().createChildNode(fan);
node1.getTransform().setTranslation(new aspose.threed.Vector3(10, 0, 0));

// Create a cylinder without a fan
var nonfan  =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
scene.getRootNode().createChildNode(nonfan);

// Save scene
scene.save("CreateFanCylinder.obj");

{{< /highlight >}}

! [Tout le monde: image_alt_text](working-with-cylinder_3.png)

Le cylindre gauche a GenerateFanCylinder = faux et celui de droite a GenerateFanCylinder = true.
