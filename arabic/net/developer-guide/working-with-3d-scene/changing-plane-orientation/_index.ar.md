---
title: Cمعلقة lane لين O
type: docs
weight: 40
url: /ar/net/changing-plane-orientation/
description: Aspose.3D for .NET يسمح بتغيير اتجاه المشهد. من أجل تغيير الاتجاه ، يتم إدخال خاصية المتجه لأعلى في فئة الطائرة.
---
##  **Cمعلقة lane لين O**
Aspose.3D for .NET يسمح بتغيير اتجاه المشهد. لتغيير الاتجاه ، تم إدخال خاصية المتجه `Up` في فئة `Plane`. يظهر مقتطف الكود التالي كيفية تغيير اتجاه الطائرة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Set Vector
scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });
//This will generate a plane that has customized orientation
scene.Save("ChangePlaneOrientation.obj");

{{< /highlight >}}
