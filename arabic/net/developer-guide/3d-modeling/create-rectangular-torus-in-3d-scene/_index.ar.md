---
title: إنشاء نتوء مستطيل في مشهد 3D
type: docs
weight: 50
url: /ar/net/create-rectangular-torus-in-3d-scene/
description: باستخدام Aspose.3D for .NET API ، يمكن للمطورين إنشاء كائنات 3D ، ثم حفظ مشهد 3D بأي تنسيق 3D مدعوم.
---
{{% alert color="primary" %}} 

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, developers can create 3D objects, and then save 3D scene in any supported 3D format.

{{% /alert %}} 
##  **Rالزاوية الأمامية orus**
We have added `RectangularTorus` class, it allows developers to place a parameterized rectangular torus into the scene, this can be converted to ordinal mesh/triangle mesh during saving the scene into different supported file formats.

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Tانه ولد توروس مستطيلة تبدو على النحو التالي:

! [Todo: image_ altttext](create-rectangular-torus-in-3d-scene_1.png)
