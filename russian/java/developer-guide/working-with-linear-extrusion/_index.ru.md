---
title: Работа с линейной экструзионной
type: docs
weight: 80
url: /ru/java/working-with-linear-extrusion/
description: Aspose.3D for Java предлагает класс LinearExtrusion, который принимает 2D форму в качестве входных данных и расширяет форму в 3-м измерении.
---
#  **Выполнение линейной экструзии**
Aspose.3D for Java предлагает класс `LinearExtrusion`, который принимает 2D форму в качестве входных данных и расширяет форму в 3-м измерении. Следующий фрагмент кода показывает, как выполнить линейную экструзию:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize the base shape to be extruded
// Initialize the base profile to be extruded
RectangleShape profile = new RectangleShape();
profile.setRoundingRadius(0.3);
// Perform Linear extrusion by passing a 2D shape as input and extend the shape in the 3rd dimension
LinearExtrusion extrusion = new LinearExtrusion(profile, 10) {{ setSlices(100); setCenter(true); setTwist(360); setTwistOffset(new Vector3(10, 0, 0));}};
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new Vector3(10, 0, 0));
// Create a scene
Scene scene = new Scene();
// Create a child node by passing extrusion
scene.getRootNode().createChildNode(extrusion);
// Save 3D scene
scene.save(MyDir +  "LinearExtrusion.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
#  **Ломтики в линейной экструзии**
Aspose.3D for Java предлагает метод `setSlices()` класса `LinearExtrusion`. Метод setSlices() определяет количество промежуточных точек вдоль пути экструзии. Следующий фрагмент кода показывает, как использовать метод setSlices() в линейной экструзии:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize the base profile to be extruded
RectangleShape profile = new RectangleShape();
profile.setRoundingRadius(0.3);
// Create a scene
Scene scene = new Scene();
// Create left node
Node left = scene.getRootNode().createChildNode();
// Create right node
Node right = scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new Vector3(5, 0, 0));

// Slices parameter defines the number of intermediate points along the path of the extrusion
// Perform linear extrusion on left node using slices property
left.createChildNode(new LinearExtrusion(profile, 2) {{setSlices(2);}});
// Perform linear extrusion on right node using slices property
right.createChildNode(new LinearExtrusion(profile, 2) {{setSlices(10);}});

// Save 3D scene
scene.save(MyDir + "SlicesInLinearExtrusion.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
#  **Центр в линейной экструзии**
Aspose.3D for Java предлагает метод `setCenter()` класса `LinearExtrusion`. Если для метода setCenter() установлено значение true, диапазон выдавливания будет от-Height/2 до Height/2, в противном случае выдавливание будет от 0 до Height. Следующий фрагмент кода показывает, как использовать метод setCenter() в линейной экструзии:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize the base profile to be extruded
RectangleShape profile = new RectangleShape();
profile.setRoundingRadius(0.3);
// Create a scene
Scene scene = new Scene();
// Create left node
Node left = scene.getRootNode().createChildNode();
// Create right node
Node right = scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new Vector3(5, 0, 0));

// If Center property is true, the extrusion range is from -Height/2 to Height/2, otherwise the extrusion is from 0 to Height
// Perform linear extrusion on left node using center and slices property
left.createChildNode(new LinearExtrusion(profile, 2) {{ setCenter(false); setSlices(3); }});
// Set ground plane for reference
left.createChildNode(new Box(0.01, 3, 3));
// Perform linear extrusion on left node using center and slices property
right.createChildNode(new LinearExtrusion(profile, 2) {{ setCenter(true); setSlices(3); }});
// Set ground plane for reference
right.createChildNode(new Box(0.01, 3, 3));

// Save 3D scene
scene.save(MyDir + "CenterInLinearExtrusion.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
#  **Твист в линейной экструзии**
Aspose.3D for Java предлагает метод `setTwist()` класса `LinearExtrusion`. Метод setTwist() обрабатывает степень вращения при выдавливании формы. Следующий фрагмент кода показывает, как использовать метод setTwist() в линейной экструзии:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize the base profile to be extruded
RectangleShape profile = new RectangleShape();
profile.setRoundingRadius(0.3);
// Create a scene
Scene scene = new Scene();
// Create left node
Node left = scene.getRootNode().createChildNode();
// Create right node
Node right = scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new Vector3(5, 0, 0));

// Twist property defines the degree of the rotation while extruding the profile
// Perform linear extrusion on left node using twist and slices property
left.createChildNode(new LinearExtrusion(profile, 10) {{ setTwist(0); setSlices(100); }});
// Perform linear extrusion on right node using twist and slices property
right.createChildNode(new LinearExtrusion(profile, 10) {{ setTwist(90); setSlices(100); }});

// Save 3D scene
scene.save(MyDir + "TwistInLinearExtrusion.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
#  **TwistOffset в линейной экструзии**
Aspose.3D for Java предлагает метод `setTwistOffset()` класса `LinearExtrusion`. Метод setTwistOffset() преобразует смещение при вращении экструзии. Следующий фрагмент кода показывает, как использовать метод setTwistOffset() в линейной экструзии:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize the base profile to be extruded
RectangleShape profile = new RectangleShape();
profile.setRoundingRadius(0.3);
        
// Create a scene
Scene scene = new Scene();
// Create left node
Node left = scene.getRootNode().createChildNode();
// Create right node
Node right = scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new Vector3(5, 0, 0));

// TwistOffset property is the translate offset while rotating the extrusion.
// Perform linear extrusion on left node using twist and slices property
left.createChildNode(new LinearExtrusion(profile, 10) {{ setTwist(360); setSlices(100); }});
// Perform linear extrusion on right node using twist, twist offset and slices property
right.createChildNode(new LinearExtrusion(profile, 10)  {{setTwist(360); setSlices(100); setTwistOffset(new Vector3(3, 0, 0));}});

// Save 3D scene
scene.save(MyDir + "TwistOffsetInLinearExtrusion.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
#  **Направление в линейной экструзии**
Aspose.3D for Java предлагает метод `setDirection()` класса `LinearExtrusion`. Метод setDirection() определяет направление выдавливания. Следующий фрагмент кода показывает, как использовать метод setDirection() в линейной экструзии:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize the base profile to be extruded
RectangleShape profile = new RectangleShape();
profile.setRoundingRadius(0.3);
// Create a scene
Scene scene = new Scene();
// Create left node
Node left = scene.getRootNode().createChildNode();
// Create right node
Node right = scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new Vector3(5, 0, 0));

// Direction property defines the direction of the extrusion.
// Perform linear extrusion on left node using twist and slices property
left.createChildNode(new LinearExtrusion(profile, 10) {{ setTwist(360); setSlices(100); }});
// Perform linear extrusion on right node using twist, slices, and direction property
right.createChildNode(new LinearExtrusion(profile, 10) {{ setTwist(360); setSlices(100); setDirection(new Vector3(0.3, 0.2, 1));}});

// Save 3D scene
scene.save(MyDir + "DirectionInLinearExtrusion.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
