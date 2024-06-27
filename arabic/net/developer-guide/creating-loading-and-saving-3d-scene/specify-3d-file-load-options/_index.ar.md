---
title: تحديد خيارات تحميل الملفات 3D بـ C#
linktitle: تحديد خيارات تحميل الملفات 3D
type: docs
weight: 30
url: /ar/net/specify-3d-file-load-options/
description: Tهنا العديد من method cene. cenطريقة القلم الزائد أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن ptions oadO. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا.
---
##  **Oفيرفيو**

توضح هذه المقالة كيف يمكنك تحميل أنواع مختلفة من ملفات 3D باستخدام فئات خيارات التحميل الخاصة بها في C# داخل كائن المشهد ثم يمكنك [حفظه بتنسيقات ملفات مختلفة مدعومة بقيمة 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). عن طريق التحميل والحفظ ، يمكنك تنفيذ عدد من التحويلات المختلفة على سبيل المثال

- تحويل FBX إلى OBJ في C#
- تحويل 3DS إلى FBX في C#
- تحويل U3D إلى OBJ في C#
- تحويل OBJ إلى 3DS في C#
- تحويل X إلى 3DS في C#

##  **خيارات تحميل الملفات 3D**
هناك العديد من الأحمال الزائدة للطرق [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) أو الأحمال الزائدة لمُنشئ فئة المشهد التي تقبل كائن `LoadOptions`. يجب أن يكون هذا موضوعًا لفئة مشتقة من فئة `LoadOptions`. يحتوي كل تنسيق تحميل على فئة مقابلة تحتوي على خيارات تحميل لتنسيق التحميل هذا ، على سبيل المثال هناك `ColladaSaveOptions` لتنسيق الحفظ `FileFormat.Collada`.
###  **استخدام خيارات التحميل السرية 3DS**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف 3DS سري.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **Use من ptions bj ptions oad ptions**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Obj 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **استخدام خيارات التحميل STL**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **استخدام خيارات التحميل U3D**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **استخدام خيارات التحميل glTF**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.
####  **Lip الشفاه V/T exexture ordinالمرؤوس**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **Use من ptions ly ptions oad ptions**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **Use من ptions iptions ptions ptions oad ptions**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **استخدام خيارات تحميل RVM**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
###  **باستخدام خيارات تحميل FBX**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
