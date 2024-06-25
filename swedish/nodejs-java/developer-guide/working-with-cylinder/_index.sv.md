---
title: Arbeta med cylinder
type: docs
weight: 100
url: /sv/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java tillåter anpassning av offset toppen av en cylinder. För att använda denna funktionalitet, kan du använda setOffsetTop () metod för cylinderklass.
---
#  **Anpassa offset övrev**
Aspose.3D for Node.js via Java tillåter anpassning av offset toppen av en cylinder. För att använda denna funktionalitet kan du använda `setOffsetTop()`-metoden för klassen `Cylinder`. Följande kod snutt visar hur man anpassar Offset Top:



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

![todo:image_alt_text](working-with-cylinder_1.png)

Den vänstra har OffsetTop satt till (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
#  **Anpassa shearBottom**
Aspose.3D for Node.js via Java tillåter anpassning av skjuv botten i en cylinder. För att kunna använda denna funktionalitet, kan du använda `setShearBottom()` egenskapen i `Cylinder` klassen. Följande kodutdrag visar hur man anpassar skjuv nedre:

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

![todo:image_alt_text](working-with-cylinder_2.png)

Den vänstra cylindern har ShearBottom till (0, 0.83) medan den högra är en vanlig cylinder.
#  **Skapa fläkt- cylinder**
Aspose.3D for Node.js via Java tillåter att skapa en fläktcylinder. För att använda denna funktionalitet, kan du `setGenerateFanCylinder()` egenskap av `Cylinder` klass till `true`. Följande kodsnutt visar hur denna funktionalitet ska användas:

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

![todo:image_alt_text](working-with-cylinder_3.png)

Den vänstra cylindern har GenerateFanCylinder = false och den högra har GenerateFanCylinder = true.
