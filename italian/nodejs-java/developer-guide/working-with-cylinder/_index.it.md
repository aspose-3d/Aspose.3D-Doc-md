---
title: Lavorare con il cilindro
type: docs
weight: 100
url: /it/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare setMetodo OffsetTop() della classe Cilindro.
---
#  **Personalizza la parte superiore offset**
Aspose.3D for Node.js via Java consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare il metodo `setOffsetTop()` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare Offset Top:



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

Quello sinistro ha OffsetTop impostato su (5, 3, 0), è facile vedere che il tappo superiore si è spostato e anche l'intero busto ne viene influenzato.
#  **Personalizza ShearBottom**
Aspose.3D for Node.js via Java consente di personalizzare il fondo di taglio di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `setShearBottom()` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare il fondo di taglio:

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

Il cilindro sinistro ha ShearBottom a (0, 0,83) mentre quello destro è un cilindro ordinale.
#  **Crea Ventilatore-Cilindro**
Aspose.3D for Node.js via Java consente di creare un cilindro della ventola. Per poter utilizzare questa funzionalità, puoi `setGenerateFanCylinder()` di proprietà della classe `Cylinder` a `true`. Il seguente frammento di codice mostra come utilizzare questa funzionalità:

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

Il cilindro sinistro ha GenerateFanCylinder = falso e quello destro ha GenerateFanCylinder = true.
