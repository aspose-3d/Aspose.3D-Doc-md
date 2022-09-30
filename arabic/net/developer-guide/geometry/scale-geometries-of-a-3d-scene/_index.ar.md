---
title: Scale هندسي من 3D cencene
type: docs
weight: 70
url: /ar/net/scale-geometries-of-a-3d-scene/
description: Dإيفلين يمكن أن مقياس هندسي فقط من عقدة 3D أو جميع العقد من 3D cenسين. In من أجل تحقيق ذلك ، يمكن للمطورين استدعاء أعضاء cale متعددة من فئة olyأوليغونوديفير سبيل المثال.
---
## **Scale هندسي عقدة واحدة 3D أو جميع العقد من 3D Scene**
Dإيفلين يمكن أن مقياس هندسي فقط من عقدة 3D أو جميع العقد من 3D cenسين. In من أجل تحقيق ذلك ، يمكن للمطورين استدعاء أعضاء cale متعددة من الدرجة `PolygonModifier` سبيل المثال. Tله هو مثال رمز لقياس جميع العقد أو عقدة واحدة:



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
