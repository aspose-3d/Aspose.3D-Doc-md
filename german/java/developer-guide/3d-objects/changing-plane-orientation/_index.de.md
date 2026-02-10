---
title: Veränderung der Flugzeug orientierung
type: docs
weight: 70
url: /de/java/changing-plane-orientation/
description: Aspose.3D for Java ermöglicht eine veränderte Ausrichtung einer Szene. Um die Ausrichtung zu ändern, werden die Methoden getUp() und setUp() in die Flugzeug klasse eingeführt.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.5 oder höher unterstützt.

{{% /alert %}} 
#  **Veränderung der Flugzeug orientierung**
Aspose.3D for Java ermöglicht eine veränderte Ausrichtung einer Szene. Um die Ausrichtung zu ändern, werden `getUp()` und `setUp()` Methoden in `Plane` Klasse eingeführt. Das folgende Code-Snippet zeigt, wie die Ausrichtung des Flugzeugs geändert wird:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
