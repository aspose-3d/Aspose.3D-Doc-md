---
title: Cambio de orientación del plano
type: docs
weight: 70
url: /es/java/changing-plane-orientation/
description: Aspose.3D for Java permite cambiar la orientación de una escena. Para cambiar la orientación, se introducen los métodos getUp() y setUp() en Plane Class.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,5 o superior.

{{% /alert %}} 
#  **Cambio de orientación del plano**
Aspose.3D for Java permite cambiar la orientación de una escena. Para cambiar la orientación, los métodos `getUp()` y `setUp()` se introducen en la clase `Plane`. El siguiente fragmento de código muestra cómo cambiar la orientación del plano:

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
