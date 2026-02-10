---
title: Hanging Plane entation rientation asılı
type: docs
weight: 70
url: /tr/java/changing-plane-orientation/
description: Aspose.3D for Java bir sahnenin değişen yönünü sağlar. Yönelimi değiştirmek için, düzlem sınıfında getup () ve kurulum () yöntemleri tanıtılır.
---
{{% alert color="primary" %}} 

This özelliği 19.5 veya daha büyük bir sürümle desteklenir.

{{% /alert %}} 
#  **Hanging Plane entation rientation asılı**
Aspose.3D for Java allows changing orientation of a scene. In order to change the orientation, `getUp()` and `setUp()` methods are introduced in `Plane` Class. Following code snippet shows how to change the plane's orientation:

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
