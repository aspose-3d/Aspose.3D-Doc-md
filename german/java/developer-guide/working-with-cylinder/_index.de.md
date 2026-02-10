---
title: Arbeiten mit Zylinder
type: docs
weight: 100
url: /de/java/working-with-cylinder/
description: Aspose.3D for Java ermöglicht das Anpassen von Offset-Oberteil eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die setOffsetTop()-Methode der Cylinder-Klasse verwenden.
---
#  **Offset-Top anpassen**
Aspose.3D for Java ermöglicht das Anpassen von Offset-Oberteil eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die `setOffsetTop()`-Methode der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Offset Top angepasst wird:



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

! [Todo: image_alt_text](working-with-cylinder_1.png)

Im linken ist OffsetTop auf (5, 3, 0) eingestellt. Es ist leicht zu erkennen, dass sich die obere Kappe bewegt hat und auch der gesamte Torso betroffen ist.
#  **Shear Bottom anpassen**
Aspose.3D for Java ermöglicht die Anpassung des Scher bodens eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `setShearBottom()` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Shear Bottom angepasst wird:



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

! [Todo: image_alt_text](working-with-cylinder_2.png)

Der linke Zylinder hat Shear Bottom bis (0, 0,83), während der rechte ein Ordnungszylinder ist.
#  **Lüfter zylinder erstellen**
Aspose.3D for Java ermöglicht die Erstellung eines Lüfter zylinders. Um diese Funktional ität nutzen zu können, können Sie `setGenerateFanCylinder()`-Eigenschaft der `Cylinder`-Klasse bis `true`. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



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

! [Todo: image_alt_text](working-with-cylinder_3.png)

Der linke Zylinder hat Generate Fan Cylinder = falsch und der rechte hat Generate Fan Cylinder = wahr.
