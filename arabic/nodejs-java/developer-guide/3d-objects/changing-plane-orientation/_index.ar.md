---
title: Cمعلقة lane لين O
type: docs
weight: 70
url: /ar/nodejs-java/changing-plane-orientation/
description: يسمح Aspose.3D for Node.js via Java بتغيير اتجاه المشهد. من أجل تغيير الاتجاه ، يتم إدخال أساليب getUp() والإعداد () في فئة الطائرة.
---
{{% alert color="primary" %}} 

هذه الميزة مدعومة بالإصدار 23.12 أو أكبر.

{{% /alert %}} 

#  **Cمعلقة lane لين O**
يسمح Aspose.3D for Node.js via Java بتغيير اتجاه المشهد. لتغيير الاتجاه ، يتم تقديم طرق `getUp()` و `setUp()` في فئة `Plane`. يظهر مقتطف الكود التالي كيفية تغيير اتجاه الطائرة:

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
