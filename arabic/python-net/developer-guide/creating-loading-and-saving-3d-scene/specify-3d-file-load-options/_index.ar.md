---
title: تحديد خيارات تحميل الملفات 3D
type: docs
weight: 30
url: /ar/python-net/specify-3d-file-load-options/
description: Tهنا العديد من method cene. cenطريقة القلم الزائد أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن ptions oadO. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا.
---
##  **خيارات تحميل الملفات 3D**
هناك العديد من الأحمال الزائدة للطرق [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) أو الأحمال الزائدة لمُنشئ فئة المشهد التي تقبل كائن `LoadOptions`. يجب أن يكون هذا موضوعًا لفئة مشتقة من فئة `LoadOptions`. يحتوي كل تنسيق تحميل على فئة مقابلة تحتوي على خيارات تحميل لتنسيق التحميل هذا ، على سبيل المثال هناك `ColladaSaveOptions` لتنسيق الحفظ `FileFormat.Collada`.
###  **استخدام خيارات التحميل السرية 3DS**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف منفصل 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Use من ptions bj ptions oad ptions**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Obj 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **استخدام خيارات التحميل STL**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **استخدام خيارات التحميل U3D**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **استخدام خيارات التحميل glTF**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.
####  **Lip الشفاه V/T exexture ordinالمرؤوس**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Use من ptions ly ptions oad ptions**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **Use من ptions iptions ptions ptions oad ptions**
Tانه رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف Diمستطيل X.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **استخدام خيارات تحميل RVM**
**C#**

```py


import aspose.threed as a3d
# set load options of RVM

scene = a3d.Scene()

opt = a3d.formats.RvmLoadOptions()
opt.cylinder_radial_segments = 32
opt.dish_latitude_segments = 16
opt.dish_longitude_segments = 24
opt.torus_tubular_segments = 40

# import RVM

scene.open("LAD-TOP.rvm", opt);

# save in the OBJ format

scene.save("LAD-TOP.obj", a3d.FileFormat.WAVEFRONT_OBJ);

```

###  **باستخدام خيارات تحميل FBX**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
