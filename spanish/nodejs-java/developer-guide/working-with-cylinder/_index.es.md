---
title: Trabajando con cilindro
type: docs
weight: 100
url: /es/nodejs-java/working-with-cylinder/
description: Aspose.3D for Node.js via Java permite personalizar Offset Top of a cylinder. Para utilizar esta funcionalidad, puede utilizar el método setOffsetTop() de la clase Cylinder.
---
#  **Personalizar parte superior offset**
Aspose.3D for Node.js via Java permite personalizar Offset Top of a cylinder. Para usar esta funcionalidad, puede usar el método `setOffsetTop()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



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

¡! [Todo: image_alt_text](working-with-cylinder_1.png)

El izquierdo tiene OffsetTop configurado en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
#  **Personalizar ShearBottom**
Aspose.3D for Node.js via Java permite personalizar el fondo de corte de un cilindro. Para usar esta funcionalidad, puede usar la propiedad `setShearBottom()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:

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

¡! [Todo: image_alt_text](working-with-cylinder_2.png)

El cilindro izquierdo tiene ShearBottom a (0, 0,83) mientras que el derecho es un cilindro ordinal.
#  **Crear ventilador-cilindro**
Aspose.3D for Node.js via Java permite crear un cilindro de ventilador. Para usar esta funcionalidad, puede `setGenerateFanCylinder()` propiedad de `Cylinder` clase a `true`. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:

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

¡! [Todo: image_alt_text](working-with-cylinder_3.png)

El cilindro izquierdo tiene GenerateFanCylinder = falso y el derecho tiene GenerateFanCylinder = true.
