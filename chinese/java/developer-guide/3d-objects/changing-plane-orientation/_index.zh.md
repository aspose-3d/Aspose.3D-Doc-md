---
title: 改变平面方向
type: docs
weight: 70
url: /zh/java/changing-plane-orientation/
description: Aspose.3D for Java 允许更改场景的方向。为了改变方向，在Plane类中引入了getUp() 和setUp() 方法。
---
{{% alert color="primary" %}} 

19.5或更高版本支持此功能。

{{% /alert %}} 
#  **改变平面方向**
Aspose.3D for Java 允许更改场景的方向。为了改变方向，在 `Plane` 类中引入了 `getUp()` 和 `setUp()` 方法。以下代码片段显示了如何更改平面的方向:

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
