---
title: Ptions pecify 3D ptions ile ptions oad ptions في C#
linktitle: Specify 3D ptions ile ile oad ptions
type: docs
weight: 30
url: /ar/net/specify-3d-file-load-options/
description: Tهنا العديد من method cene. cenطريقة القلم الزائد أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن ptions oadO. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا.
---
## **Oفيرفيو**

Tمقالته يشرح كيف يمكنك تحميل أنواع مختلفة من الملفات 3D باستخدام الطبقات خيار تحميل كل منها في C# داخل الكائن cencene ومن ثم يمكنك[حفظه في تنسيقات الملفات المدعومة 3D المختلفة](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). By التحميل saving ، يمكنك تنفيذ عدد من التحويلات المختلفة على سبيل المثال

- Convert FBX إلى OBJ في C#
- Convert 3DS إلى FBX في C#
- Convert U3D إلى OBJ في C#
- Convert OBJ إلى 3DS في C#
- Convert X إلى 3DS في C#

## **3D ptions ile ptions oad ptions**
في ما يلي العديد من [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) طريقة الأحمال الزائدة أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن `LoadOptions`. Tيجب أن يكون كائن من فئة مشتقة من فئة `LoadOptions`. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا ، على سبيل المثال هناك `ColladaSaveOptions` لتنسيق حفظ `FileFormat.Collada`.
### **Use من ptions iscreet 3DS ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Use من ptions bj ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف 3D Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Use من STL ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Use من U3D ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Use من glTF ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.
#### **Lip الشفاه V/T exexture ordinالمرؤوس**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Use من ptions ly ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Use من DirectX ptions ptions oad ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Use RVM خيارات التحميل**
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
### **Using FBX ptions oad ptions**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
