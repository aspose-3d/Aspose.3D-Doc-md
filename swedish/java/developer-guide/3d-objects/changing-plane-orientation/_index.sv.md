---
title: Ändra planorientering
type: docs
weight: 70
url: /sv/java/changing-plane-orientation/
description: Aspose.3D for Java tillåter ändrad orientering av en scen. För att ändra riktningen introduceras getUp() och setUp() metoder i Plane Class.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.5 eller större.

{{% /alert %}} 
#  **Ändra planorientering**
Aspose.3D for Java tillåter ändrad orientering av en scen. För att ändra orienteringen introduceras `getUp()` och `setUp()` metoder i `Plane` klass. Följande kodsnutt visar hur man ändrar planets orientering:

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
