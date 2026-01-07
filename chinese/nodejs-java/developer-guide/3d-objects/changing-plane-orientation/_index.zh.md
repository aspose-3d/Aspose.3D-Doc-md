---
title: 改变平面方向
type: docs
weight: 70
url: /zh/nodejs-java/changing-plane-orientation/
description: Aspose.3D for Node.js via Java 允许更改场景的方向。为了改变方向，在Plane类中引入了getUp() 和setUp() 方法。
---
{{% alert color="primary" %}} 

版本23.12或更高版本支持此功能。

{{% /alert %}} 

#  **改变平面方向**
Aspose.3D for Node.js via Java 允许更改场景的方向。为了改变方向，在 `Plane` 类中引入了 `getUp()` 和 `setUp()` 方法。以下代码片段显示了如何更改平面的方向:

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize Scene
var scene = new aspose.threed.Scene();

// Initialize Plane
var plane=new aspose.threed.Plane();

// Set Vector
plane.setUp(new aspose.threed.Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);

//This will generate a plane that has customized orientation
scene.save("ChangePlaneOrientation.obj");

{{< /highlight >}}
