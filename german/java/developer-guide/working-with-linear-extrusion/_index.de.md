---
title: Arbeiten mit linearer Extrusion
type: docs
weight: 80
url: /de/java/working-with-linear-extrusion/
description: Aspose.3D for Java bietet LinearExtrusion-Klasse, die eine 2D-Form als Eingabe annimmt und die Form in der 3. Dimension erweitert.
---
#  **Lineare Extrusion durchführen**
Aspose.3D for Java bietet `LinearExtrusion` Klasse, die eine 2D-Form als Eingabe annimmt und die Form in der 3. Dimension erweitert. Das folgende Code-Snippet zeigt, wie eine lineare Extrusion durchgeführt wird:

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
#  **Scheiben in der linearen Extrusion**
Aspose.3D for Java bietet `setSlices()` Methode der `LinearExtrusion` Klasse. Set Slices() Methode definiert die Anzahl der Zwischen punkte entlang des Pfades der Extrusion. Das folgende Code-Snippet zeigt, wie die setSlices()-Methode bei der linearen Extrusion verwendet wird:

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
#  **Zentrum in der linearen Extrusion**
Aspose.3D for Java bietet `setCenter()` Methode der `LinearExtrusion` Klasse. Wenn die set Center()-Methode auf true gesetzt ist, reicht der Extrusion bereich von-Höhe/2 bis Höhe/2, andernfalls ist die Extrusion von 0 bis Höhe. Das folgende Code-Snippet zeigt, wie die setCenter()-Methode bei der linearen Extrusion verwendet wird:

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
#  **Twist in der linearen Extrusion**
Aspose.3D for Java bietet `setTwist()` Methode der `LinearExtrusion` Klasse. Die set Twist()-Methode behandelt den Grad der Rotation, während die Form extrudiert wird. Das folgende Code-Snippet zeigt, wie die setTwist()-Methode bei der linearen Extrusion verwendet wird:

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
#  **Twist Offset in linearer Extrusion**
Aspose.3D for Java bietet `setTwistOffset()` Methode der `LinearExtrusion` Klasse. Die setTwist Offset()-Methode übersetzt den Offset beim Drehen der Extrusion. Das folgende Code-Snippet zeigt, wie die setTwist Offset()-Methode bei der linearen Extrusion verwendet wird:

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
#  **Richtung in linearer Extrusion**
Aspose.3D for Java bietet `setDirection()` Methode der `LinearExtrusion` Klasse. Die setDirection()-Methode definiert die Richtung der Extrusion. Das folgende Code-Snippet zeigt, wie die setDirection()-Methode bei der linearen Extrusion verwendet wird:

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
