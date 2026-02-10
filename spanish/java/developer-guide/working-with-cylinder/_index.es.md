---
title: Trabajando con cilindro
type: docs
weight: 100
url: /es/java/working-with-cylinder/
description: Aspose.3D for Java permite personalizar Offset Top of a cylinder. Para utilizar esta funcionalidad, puede utilizar el método setOffsetTop() de la clase Cylinder.
---
#  **Personalizar parte superior offset**
Aspose.3D for Java permite personalizar Offset Top of a cylinder. Para usar esta funcionalidad, puede usar el método `setOffsetTop()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Create a scene
Scene scene = new Scene();
// Initialize cylinder
Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Set OffsetTop
cylinder1.setOffsetTop(new Vector3(5, 3, 0));
// Create ChildNode
scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);
// Initialize second cylinder without customized OffsetTop
Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Create ChildNode
scene.getRootNode().createChildNode(cylinder2);
// Save
scene.save(RunExamples.getDataDir()+ "CustomizedOffsetTopCylinder.obj", FileFormat.WAVEFRONTOBJ);
{{< /highlight >}}

¡! [Todo: image_alt_text](working-with-cylinder_1.png)

El izquierdo tiene OffsetTop configurado en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
#  **Personalizar ShearBottom**
Aspose.3D for Java permite personalizar el fondo de corte de un cilindro. Para usar esta funcionalidad, puede usar la propiedad `setShearBottom()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Create a scene
Scene scene = new Scene();
// Create cylinder 1
Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Customized shear bottom for cylinder 1
cylinder1.setShearBottom(new Vector2(0, 0.83));// shear 47.5deg in xy plane(z-axis)
// Add cylinder 1 to the scene
scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);
// Create cylinder 2
Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Add cylinder to without a ShearBottom to the scene
scene.getRootNode().createChildNode(cylinder2);
// Save scene
scene.save(RunExamples.getDataDir()+ "CustomizedShearBottomCylinder.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

¡! [Todo: image_alt_text](working-with-cylinder_2.png)

El cilindro izquierdo tiene ShearBottom a (0, 0,83) mientras que el derecho es un cilindro ordinal.
#  **Crear ventilador-cilindro**
Aspose.3D for Java permite crear un cilindro de ventilador. Para utilizar esta funcionalidad, puede `setGenerateFanCylinder()` propiedad de `Cylinder` clase a `true`. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Jav
// Create a Scene
Scene scene = new Scene();
// Create a cylinder
Cylinder fan = new Cylinder(2, 2, 10, 20, 1, false);
// Set GenerateGanCylinder to true
fan.setGenerateFanCylinder(true);
// Set ThetaLength
fan.setThetaLength(MathUtils.toRadian(270.0));
// Create ChildNode
scene.getRootNode().createChildNode(fan).getTransform().setTranslation(10, 0, 0);
// Create a cylinder without a fan
Cylinder nonfan = new Cylinder(2, 2, 10, 20, 1, false);
// Create ChildNode
scene.getRootNode().createChildNode(nonfan);
// Save scene
scene.save(RunExamples.getDataDir()+ "CreateFanCylinder.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

¡! [Todo: image_alt_text](working-with-cylinder_3.png)

El cilindro izquierdo tiene GenerateFanCylinder = falso y el derecho tiene GenerateFanCylinder = true.
