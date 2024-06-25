---
title: Working مع Cيندر
type: docs
weight: 130
url: /ar/python-net/working-with-cylinder/
description: يسمح Aspose.3D for Python via .NET بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية الإزاحة لفئة الأسطوانة.
---
#  **Customize ffffset op op**
يسمح Aspose.3D for Python via .NET بتخصيص أعلى إزاحة للأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية `offset` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أعلى الإزاحة:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

! [Todo: image_ altttext](working-with-cylinder_1.png)

تم ضبط `offset_top` على اليسار (5 ، 3 ، 0) ، ومن السهل رؤية أن الغطاء العلوي قد تحرك وأن الجذع بأكمله قد تأثر أيضًا.
#  **Customize hearالموقد العثماني**
يسمح Aspose.3D for Python via .NET بتخصيص أسفل قص الأسطوانة. من أجل استخدام هذه الوظيفة ، يمكنك استخدام خاصية `shear_bottom` من فئة `Cylinder`. يوضح مقتطف الكود التالي كيفية تخصيص أسفل القص:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Todo: image_ altttext](working-with-cylinder_2.png)

The left cylinder has `shear_bottom` to (0, 0.83) while the right one is an ordinal cylinder.
#  **Create an an-Cylinder**
Aspose.3D for Python via .NET يسمح بإنشاء أسطوانة مروحة. من أجل استخدام هذه الوظيفة ، يمكنك تعيين خاصية `generate_fan_cylinder` لفئة `Cylinder` إلى `True`. يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Todo: image_ altttext](working-with-cylinder_3.png)

تحتوي الأسطوانة اليسرى على `generate_fan_cylinder = False` ولدى الأسطوانة اليمنى `generate_fan_cylinder = True`.
