---
title: أشكال هندسية بمقياس لمشهد 3D
type: docs
weight: 70
url: /ar/net/scale-geometries-of-a-3d-scene/
description: يمكن للمطورين قياس الأشكال الهندسي فقط بعقدة 3D أو جميع عُقد مشهد 3D. من أجل تحقيق ذلك ، يمكن للمطورين استدعاء أعضاء نطاق متعددة من مثيل فئة PolygonModifier.
---
##  **أشكال أشكال أشكال حجم عقدة واحدة 3D أو جميع عُقد مشهد 3D**
يمكن للمطورين قياس الأشكال الهندسي فقط بعقدة 3D أو جميع عُقد مشهد 3D. من أجل تحقيق ذلك ، يمكن للمطورين استدعاء عدة أعضاء مقياس في مثيل فئة `PolygonModifier`. هذا هو مثال رمز لتوسيع نطاق جميع العقد أو عقدة واحدة:



**C#**

{{< highlight "java" >}}

 // scale the model in huge-scene.obj by 0.01 and save it to another file:

Scene scene = new Scene("huge-scene.obj");

// create a Box instance

var box = scene.RootNode.CreateChildNode("box", new Box());

// scale geometries of a single node

PolygonModifier.Scale(box, new Vector3(0.01));

// scale geometries of all nodes

PolygonModifier.Scale(scene, new Vector3(0.01));

scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
