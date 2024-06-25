---
title: Working مع Linear Extrusion
type: docs
weight: 110
url: /ar/python-net/working-with-linear-extrusion/
description: يقدم Aspose.3D for Python via .NET فئة LinearExtrusion ، والتي تأخذ شكل 2D كمدخل وتمتد الشكل في البعد الثالث.
---
#  **Pتشكيل Lineinextrusion**
يقدم Aspose.3D for Python via .NET فئة `LinearExtrusion` ، والتي تأخذ شكل ثنائي الأبعاد كمدخل وتطيل الشكل في البعد الثالث. يظهر مقتطف الكود التالي كيفية إجراء البثق الخطي:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-LinearExtrusion-PerformingLinearExtrusion-PerformingLinearExtrusion.py" >}}
#  **"الشقوق" في Linear xxtrusion**
Aspose.3D for Python via .NET offers `slices` property of `LinearExtrusion` class. `slices` property defines the number of intermediate points along the path of the extrusion. Following code snippet shows how to use `slices` property in linear extrusion:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-LinearExtrusion-SlicesInLinearExtrusion-SlicesInLinearExtrusion.py" >}}
#  **"محور" في Linear Extrusion**
يوفر Aspose.3D for Python via .NET خاصية `center` من فئة `LinearExtrusion`. إذا تم تعيين الخاصية `center` إلى `True` ، يكون نطاق البثق من-الارتفاع/2 إلى الارتفاع/2 ، وإلا فإن البثق من 0 إلى الارتفاع. يوضح مقتطف الكود التالي كيفية استخدام خاصية `center` في البثق الخطي:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-LinearExtrusion-SlicesInLinearExtrusion-SlicesInLinearExtrusion.py" >}}
#  **'التواء' في Linear Extrusion**
يوفر Aspose.3D for Python via .NET خاصية `twist` من فئة `LinearExtrusion`. تعالج الخاصية `twist` درجة الدوران بينما تنبثق الشكل. يوضح مقتطف الكود التالي كيفية استخدام خاصية `twist` في البثق الخطي:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-LinearExtrusion-TwistInLinearExtrusion-TwistInLinearExtrusion.py" >}}
#  **'تويست _ خارج' في LineExtrusion**
Aspose.3D for Python via .NET offers `twist_offset` property of `LinearExtrusion` class. `twist_offset` property translates offset while rotating the extrusion. Following code snippet shows how to use `twist_offset` property in linear extrusion:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-LinearExtrusion-TwistOffsetInLinearExtrusion-TwistOffsetInLinearExtrusion.py" >}}
#  **'الإخراج' في Linear Extrusion**
Aspose.3D for Python via .NET offers `direction` property of `LinearExtrusion` class. `direction` property defines the direction of the extrusion. Following code snippet shows how to use `direction` property in linear extrusion:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-LinearExtrusion-DirectionInLinearExtrusion-DirectionInLinearExtrusion.py" >}}
