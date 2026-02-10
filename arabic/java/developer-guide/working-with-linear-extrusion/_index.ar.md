---
title: Working مع Linear Extrusion
type: docs
weight: 80
url: /ar/java/working-with-linear-extrusion/
description: Aspose.3D for Java تقدم فئة triearextrusion ، والتي تأخذ شكل ثنائي الأبعاد كمدخل وتمتد الشكل في البعد الثالث.
---
#  **Pتشكيل Lineinextrusion**
Aspose.3D for Java يقدم فئة `LinearExtrusion` ، والتي تأخذ شكل ثنائي الأبعاد كمدخل وتطيل الشكل في البعد الثالث. يظهر مقتطف الكود التالي كيفية إجراء البثق الخطي:

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
#  **Ices ices في Linextrusion**
Aspose.3D for Java يوفر طريقة `setSlices()` لفئة `LinearExtrusion`. تحدد طريقة setSlices() عدد النقاط الوسيطة على طول مسار البثق. يظهر مقتطف الكود التالي كيفية استخدام طريقة setSlices() في البثق الخطي:

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
#  **Cأدخل في Linear Extrusion**
Aspose.3D for Java يوفر طريقة `setCenter()` لفئة `LinearExtrusion`. إذا تم تعيين طريقة setCenter() على true ، يكون نطاق البثق من-الارتفاع/2 إلى الارتفاع/2 ، وإلا ، يكون البثق من 0 إلى الارتفاع. يوضح مقتطف الكود التالي كيفية استخدام طريقة setCenter() في البثق الخطي:

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
#  **Twist في Linear xxtrusion**
Aspose.3D for Java يوفر طريقة `setTwist()` لفئة `LinearExtrusion`. تتعامل طريقة setTwist() مع درجة الدوران أثناء بثق الشكل. يوضح مقتطف الكود التالي كيفية استخدام طريقة setTwist() في البثق الخطي:

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
#  **FfwistOffset في Linear xxtrusion**
Aspose.3D for Java يوفر طريقة `setTwistOffset()` لفئة `LinearExtrusion`. طريقة setTwistOffset() تترجم الإزاحة أثناء تدوير البثق. يظهر مقتطف الكود التالي كيفية استخدام طريقة setTwistOffset() في البثق الخطي:

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
#  **Direction في Linear Extrusion**
Aspose.3D for Java يوفر طريقة `setDirection()` لفئة `LinearExtrusion`. تحدد طريقة setDirection() اتجاه البثق. يوضح مقتطف الكود التالي كيفية استخدام طريقة setDirection() في البثق الخطي:

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
