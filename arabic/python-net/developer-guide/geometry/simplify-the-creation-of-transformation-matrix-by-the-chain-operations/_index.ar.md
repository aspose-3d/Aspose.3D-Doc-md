---
title: Impيمس إنشاء مصفوفة التحول من قبل عمليات السلسلة
type: docs
weight: 60
url: /ar/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: يقدم Aspose.3D for Python via .NET API فئة TransformBuilder التي تبسط إنشاء مصفوفة التحويل بواسطة عمليات السلسلة.
---
{{% alert color="primary" %}} 

يوفر Aspose.3D for Python via .NET API فئة `TransformBuilder` التي تبسط إنشاء مصفوفة التحويل بواسطة عمليات السلسلة.

{{% /alert %}} 

افترض أن هناك مثيل `TransformBuilder`**السل**، وعمليات السلسلة:

**Python**

```py

import aspose.threed as a3d

# Change the (x, y, z) into (x + 1, y, z)

tb = a3d.utilities.TransformBuilder(a3d.utilities.ComposeOrder.APPEND)

a = tb.translate(1, 0, 0)
# Rotate alone with the Y axis with 180 deg will change the (x, y, z) into (-x, y, -z)
.rotate_euler_degree(0, 180, 0)
# Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
.scale(2)
# change the (x, y, z) into (z, y, x)
.rearrange(a3d.Axis.Z_AXIS, a3d.Axis.Y_AXIS, a3d.Axis.X_AXIS)
.matrix


```

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

**Python**

```py

import aspose.threed as a3d

# use prepend order so the calculation is performed from left to right:
m = (a3d.utilities.TransformBuilder(a3d.utilities.ComposeOrder.PREPEND))
   # Change the (x, y, z) into (x + 1, y, z)
   .translate(1, 0, 0)
   # Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
   .rotate_euler_degree(0, 180, 0)
   # Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
   .scale(2)
   # change the (x, y, z) into (z, y, x)
   .rearrange(a3d.Axis.Z_AXIS, a3d.Axis.Y_AXIS, a3d.Axis.X_AXIS)
   .matrix
# Apply this matrix on a (0, 0, 0) vector, then we get the right result (0, 0, -2)
 t = m * a3d.utilities.Vector3.ORIGIN;

```

{{% alert color="primary" %}} 

الطرق الجديدة المضافة في فئات `Matrix4` و `TransformBuilder` هي الأدوات المساعدة للمطورين لنموذج المشهد حسب البرنامج ، لذلك لا يحتاجون إلى إنشاء مصفوفة التحويل يدويًا ، وعادة ما يستخدم المطورون الخبراء هذا.

يمكن للمطورين الترتيبيين استخدام خاصية `Transform` لفئة `Node` لتغيير ترجمة/تحجيم/تدوير كائن ما.

يمكن للمطورين أيضًا تعيين المصفوفة التي أنشأها `TransformBuilder` إلى `Node.Transform`.

يمكن العثور على مزيد من المعلومات حول مصفوفة التحويل على Wikipedia [مصفوفة رانسفورميشن](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) و [Aفين ranransofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
