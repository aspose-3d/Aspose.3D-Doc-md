---
title: Create مستطيلة Torus في 3D cencene
type: docs
weight: 50
url: /ar/net/create-rectangular-torus-in-3d-scene/
description: Sing sing Aspose.3D for .NET API ، يمكن للمطورين إنشاء الأشياء 3D ، ومن ثم حفظ المشهد 3D في أي تنسيق معتمد 3D.
---
{{% alert color="primary" %}} 

Uالغناء[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API ، يمكن للمطورين إنشاء أشياء 3D ، ثم حفظ 3D المشهد في أي تنسيق 3D المدعومة.

{{% /alert %}} 
## **Rالزاوية الأمامية orus**
Added e أضافت `RectangularTorus` الفئة ، فإنه يسمح للمطورين لوضع توروس مستطيلة متناظرة في المشهد ، وهذا يمكن تحويلها إلى شبكة/مثلث شبكة عادية أثناء حفظ المشهد في تنسيقات الملفات المدعومة المختلفة.

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

![تودو: الصورة_البديل_نص](create-rectangular-torus-in-3d-scene_1.png)
