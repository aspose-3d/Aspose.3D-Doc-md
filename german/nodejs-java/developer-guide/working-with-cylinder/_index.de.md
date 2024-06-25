---
title: Arbeiten mit Zylinder
type: docs
weight: 100
url: /de/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java ermöglicht das Anpassen von Offset Top eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die setOffsetTop()-Methode der Cylinder-Klasse verwenden.
---
#  **Offset-Top anpassen**
Aspose.3D for Node.js via Java ermöglicht das Anpassen von Offset Top eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die `setOffsetTop()`-Methode der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Offset Top angepasst wird:



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

! [Todo: image_alt_text](working-with-cylinder_1.png)

Im linken ist OffsetTop auf (5, 3, 0) eingestellt. Es ist leicht zu erkennen, dass sich die obere Kappe bewegt hat und auch der gesamte Torso betroffen ist.
#  **Shear Bottom anpassen**
Aspose.3D for Node.js via Java ermöglicht die Anpassung des Scher bodens eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `setShearBottom()` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Shear Bottom angepasst wird:

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

! [Todo: image_alt_text](working-with-cylinder_2.png)

Der linke Zylinder hat Shear Bottom bis (0, 0,83), während der rechte ein Ordnungszylinder ist.
#  **Lüfter zylinder erstellen**
Aspose.3D for Node.js via Java ermöglicht die Erstellung eines Lüfter zylinders. Um diese Funktional ität nutzen zu können, können Sie `setGenerateFanCylinder()`-Eigenschaft der `Cylinder`-Klasse bis `true`. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:

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

! [Todo: image_alt_text](working-with-cylinder_3.png)

Der linke Zylinder hat Generate Fan Cylinder = falsch und der rechte hat Generate Fan Cylinder = wahr.
