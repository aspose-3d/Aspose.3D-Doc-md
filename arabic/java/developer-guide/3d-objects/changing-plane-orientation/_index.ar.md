---
title: Cمعلقة lane لين O
type: docs
weight: 70
url: /ar/java/changing-plane-orientation/
description: Aspose.3D for Java يسمح بتغيير اتجاه المشهد. من أجل تغيير الاتجاه ، يتم إدخال أساليب getUp() والإعداد () في فئة الطائرة.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.5 أو أكبر.

{{% /alert %}} 
#  **Cمعلقة lane لين O**
Aspose.3D for Java يسمح بتغيير اتجاه المشهد. لتغيير الاتجاه ، يتم تقديم طرق `getUp()` و `setUp()` في فئة `Plane`. يظهر مقتطف الكود التالي كيفية تغيير اتجاه الطائرة:

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
