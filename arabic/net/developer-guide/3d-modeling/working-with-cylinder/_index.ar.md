---
title: Working مع Cيندر
type: docs
weight: 130
url: /ar/net/working-with-cylinder/
description: Aspose.3D for .NET يسمح بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية الإزاحة لفئة الأسطوانة.
---
#  **Customize ffffset op op**
Aspose.3D for .NET يسمح بتخصيص أعلى إزاحة للأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام خاصية `Offset` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أعلى الإزاحة:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

! [Todo: image_ altttext](working-with-cylinder_1.png)

Tترك واحد لديه ffffsetTop مجموعة إلى (5 ، 3 ، 0) ، فإنه من السهل أن نرى الغطاء العلوي قد انتقلت والجذع كله أيضا يتأثر.
#  **Customize hearالموقد العثماني**
Aspose.3D for .NET يسمح بتخصيص قاع قص الأسطوانة. لاستخدام هذه الوظيفة ، يمكنك استخدام خاصية `ShearBottom` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أسفل القص:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Todo: image_ altttext](working-with-cylinder_2.png)

The left cylinder has `ShearBottom` to (0, 0.83) while the right one is an ordinal cylinder.
#  **Create an an-Cylinder**
Aspose.3D for .NET يسمح بإنشاء أسطوانة مروحة. من أجل استخدام هذه الوظيفة ، يمكنك تعيين خاصية `GenerateFanCylinder` لفئة `Cylinder` على `true`. يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Todo: image_ altttext](working-with-cylinder_3.png)

تحتوي الأسطوانة اليسرى على `GenerateFanCylinder = false` ولدى الأسطوانة اليمنى `GenerateFanCylinder = true`.
