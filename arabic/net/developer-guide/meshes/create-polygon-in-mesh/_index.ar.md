---
title: Cريت Pأوليغون In Msh
type: docs
weight: 14
url: /ar/net/create-polygon-in-mesh/
description: Aspose.3D for .NET يسمح بإنشاء مضلع في شبكة. من أجل استخدام الوظيفة ، يقدم API طريقة CreatePolygon لفئة الشبكات.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 
##  **Cريت Pأوليغون In Msh**
Aspose.3D for .NET يسمح بإنشاء مضلع في شبكة. من أجل استخدام الوظيفة ، يقدم API طريقة [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) لفئة [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). باستخدام طريقة CreatePolygon ، يمكنك إنشاء مضلع محسن [Riريانجل](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) أو [Qواد](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) دون تخصيص ذاكرة إضافية. يوضح مقتطف الرمز التالي كيفية استخدام هذه الوظيفة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
