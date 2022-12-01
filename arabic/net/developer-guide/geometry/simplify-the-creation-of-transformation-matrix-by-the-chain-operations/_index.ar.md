---
title: Impيمس إنشاء مصفوفة التحول من قبل عمليات السلسلة
type: docs
weight: 60
url: /ar/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API يقدم فئة ranransformBuilder الذي يبسط إنشاء مصفوفة التحول من خلال عمليات السلسلة.
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API يقدم فئة `TransformBuilder` الذي يبسط إنشاء مصفوفة التحول من خلال عمليات السلسلة.

{{% /alert %}} 

Suppose ، هناك مثيل غير رسمي uilder**السل**، وعمليات السلسلة:

**C#**

{{< highlight "java" >}}

 // Change the (x, y, z) into (x + 1, y, z)

var a = tb.Translate(1, 0, 0)

// Rotate alone with the Y axis with 180 deg will change the (x, y, z) into (-x, y, -z)

.RotateEulerDegree(0, 180, 0)

// Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)

.Scale(2)

// change the (x, y, z) into (z, y, x)

.Rearrange(Axis.ZAxis, Axis.YAxis, Axis.XAxis)

.Matrix;



public enum ComposeOrder

{

   /// <summary>

   /// Append the new transform to the chain

   /// </summary>

   Append,

   /// <summary>

   /// Prepend the new transform to the chain

   /// </summary>

   Prepend

}

{{< /highlight >}}

إذا كان ترتيب التأليف لهذا المثال هو التوبة ، يتم حساب المصفوفة النهائية من اليسار إلى اليمين ، وهذا يعني أن مصفوفة التحول النهائي سوف تفعل هذه المهام:

1. Change و (x ، y ، z) إلى (x 1 ، y ، z)
1. Rotate وحدها مع محور Y مع 180deg سوف تغير (x ، y ، z) إلى (-x ، y ،-z)
1. سوف Scale by 2 تغيير (x ، y ، z) إلى (2x ، 2y ، 2z)
1. Change و (x ، y ، z) إلى (z ، y ، x)

But إذا كان الطلب تأليف هو Append ، سيتم عكس الطلب مثل:

1. Change و (x ، y ، z) إلى (z ، y ، x)
1. سوف Scale by 2 تغيير (x ، y ، z) إلى (2x ، 2y ، 2z)
1. Rotate وحدها مع محور Y مع 180deg سوف تغير (x ، y ، z) إلى (-x ، y ،-z)
1. Change و (x ، y ، z) إلى (x 1 ، y ، z)

**C#**

{{< highlight "java" >}}

 //use prepend order so the calculation is performed from left to right:

var m = (new TransformBuilder(ComposeOrder.Prepend))

   //Change the (x, y, z) into (x + 1, y, z)

   .Translate(1, 0, 0)

   // Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)

   .RotateEulerDegree(0, 180, 0)

   //Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)

   .Scale(2)

   //change the (x, y, z) into (z, y, x)

   .Rearrange(Axis.ZAxis, Axis.YAxis, Axis.XAxis)

   .Matrix;

 //Apply this matrix on a (0, 0, 0) vector, then we get the right result (0, 0, -2)

 var t = m * Vector3.Origin;

{{< /highlight >}}

{{% alert color="primary" %}} 

Tوأضاف أساليب جديدة في الطبقات `Matrix4` و `TransformBuilder` هي المرافق للمطورين لنموذج المشهد عن طريق البرنامج ، لذلك لا تحتاج إلى بناء يدويا مصفوفة التحويل ، وعادة ما يستخدم هذا من قبل المطورين الخبراء.

يمكن للمطورين dinal rdial استخدام خاصية `Transform` من الفئة `Node` لتغيير الترجمة/التحجيم/دوران الكائن.

Dإيفلين يمكن أيضا تعيين مصفوفة التي أنشأتها `TransformBuilder` إلى `Node.Transform`.

يمكن العثور على معلومات خام Mحول مصفوفة التحول في Wikipedia[مصفوفة رانسفورميشن](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics)و[Aفين ranransofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
