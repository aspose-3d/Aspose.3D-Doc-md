---
title: Cريت Pأوليغون In Msh
type: docs
weight: 80
url: /ar/java/create-polygon-in-mesh/
description: Aspose.3D for Java يسمح بإنشاء مضلع في شبكة.
---
##  **Cريت Pأوليغون In Msh**
Aspose.3D for Java يسمح بإنشاء مضلع في شبكة. من أجل استخدام الوظيفة ، يقدم API طريقة [CreatePأوليغون](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) لفئة [Mإيش](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). باستخدام طريقة CreatePolygon ، يمكنك إنشاء مضلع محسن [Riريانجل](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) أو [Qواد](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) دون تخصيص ذاكرة إضافية. يوضح مقتطف الرمز التالي كيفية استخدام هذه الوظيفة.



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize Mesh
Mesh mesh = new Mesh();
//The old CreatePolygon needs to create a temporary array for holding the face indices
//mesh.createPolygon(new int[] { 0, 1, 2 });
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);
//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
