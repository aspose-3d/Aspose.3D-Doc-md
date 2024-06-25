---
title: Cريت Pأوليغون In Msh
type: docs
weight: 80
url: /ar/nodejs-java/create-polygon-in-mesh/
description: يسمح Aspose.3D for Node.js via Java بإنشاء مضلع في شبكة.
---
##  **Cريت Pأوليغون In Msh**
يسمح Aspose.3D for Node.js via Java بإنشاء مضلع في شبكة. من أجل استخدام الوظيفة ، يقدم API طريقة [CreatePأوليغون](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) لفئة [Mإيش](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh). باستخدام طريقة CreatePolygon ، يمكنك إنشاء مضلع محسن [Riريانجل](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-) أو [Qواد](https://reference.aspose.com/3d/java/com.aspose.threed/Mesh#createPolygon-int-int-int-int-) دون تخصيص ذاكرة إضافية. يوضح مقتطف الرمز التالي كيفية استخدام هذه الوظيفة.



{{< highlight "java" >}}

// Initialize Mesh
var mesh = new aspose.threed.Mesh();

//The old CreatePolygon needs to create a temporary array for holding the face indices
//The new overloads doesn't need extra allocation, and it's optimized internally.
mesh.createPolygon(0, 1, 2);

//Or You can create a polygon using 4 vertices(quad)
//mesh.createPolygon(0, 1, 2, 3);

{{< /highlight >}}
