---
title: Changer l'orientation de l'avion
type: docs
weight: 70
url: /fr/java/changing-plane-orientation/
description: Aspose.3D for Java permet de changer l'orientation d'une scène. Afin de changer l'orientation, les méthodes getUp() et setUp() sont introduites dans Plane Class.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.5 ou supérieure.

{{% /alert %}} 
#  **Changer l'orientation de l'avion**
Aspose.3D for Java permet de changer l'orientation d'une scène. Afin de changer l'orientation, les méthodes `getUp()` et `setUp()` sont introduites dans la classe `Plane`. L'extrait de code suivant montre comment modifier l'orientation du plan:

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
