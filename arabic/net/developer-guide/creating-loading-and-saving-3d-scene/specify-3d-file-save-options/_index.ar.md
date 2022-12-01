---
title: Ptions pecify 3D ptions ile ile ave ptions في C#
linktitle: Specify 3D ile ile ile ave ptions
type: docs
weight: 40
url: /ar/net/specify-3d-file-save-options/
description: Tهنا العديد من طريقة cencene. cenave الزائدة التي تقبل كائن ptions aveO. Each حفظ تنسيق لديه فئة المقابلة التي تحمل خيارات حفظ لهذا تنسيق حفظ.
---
## **Oفيرفيو**

Tمقالته يشرح كيف يمكنك حفظ الملفات 3D في صيغ مختلفة[بعد تحميلها في كائن Scene](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)باستخدام C#. By التحميل saving ، يمكنك تنفيذ عدد من التحويلات المختلفة على سبيل المثال

- Convert FBX إلى X في C#
- Convert GLTF إلى OBJ في C#
- Convert OBJ إلى X في C#
- Convert STL إلى OBJ في C#
- Convert RVM إلى 3DS في C#

## **3D ptions ile ptions ave ptions**
Tهنا العديد من طريقة [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) الزائدة التي تقبل كائن aveOptions. Tيجب أن يكون كائن من فئة مشتقة من فئة `SaveOptions`. Each حفظ تنسيق لديه فئة المقابلة التي تحمل خيارات حفظ لهذا تنسيق حفظ ، على سبيل المثال ، هناك `ColladaSaveOptions` لصيغة حفظ `FileFormat.Collada`.
### **Use من Collada ptions ave ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات حفظ قبل حفظ ملف 3D إلى تنسيق Collada.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Use من Discreet3DS ptions ave ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات حفظ قبل حفظ ملف 3D إلى تنسيق iscreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Use من FBX ptions ave ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات حفظ قبل حفظ ملف 3D إلى تنسيق FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

يعرض `FBXSaveOptions` أيضًا خاصية `EnableCompression` التي يمكن استخدامها لضغط البيانات الثنائية الكبيرة في ملف FBX. قيمة Default لهذه الخاصية صحيحة. Below رمز قنص يشرح كيف يمكنك العمل مع هذه الخاصية مع توفير مشهد.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Use من ptions bj ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق bj O.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Use من STL ptions ave ptions**
The C# رمز أدناه يظهر كيفية تعيين خيارات حفظ قبل حفظ ملف 3D إلى تنسيق STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Use من U3D ptions ave ptions**
The C# رمز أدناه يوضح كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Use من glTF ptions ave ptions**
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 



The C# رمز أدناه يوضح كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق glTF.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **PrettyPrint in glTF ptions ave ptions**
You يمكن أيضا استخدام خاصية rerettyPrint من GLclass class avaveOفئة الوصفات لطباعة human understandunderstandالإنسان. Tانه رمز أدناه يظهر كيفية استخدام هذه الوظيفة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Cies ave epepencies من 3D cencene في cenial ile ile yالجذعية**
قد تتطلب opers evelحفظ جميع اعتمادات المشهد 3D في نظام الملفات الحقيقي. Tيا يمكن تحديد مسار دليل محلي ، حفظ في الكائن `MemoryFileSystem` أو ببساطة تجاهل التبعيات. Tهو `FileSystem` يتم إضافة الممتلكات في جميع الطبقات خيار حفظ.
#### **Discard aving aving المواد iles iles**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Cies ave epفي Lثماني D**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **Cies افي epependenفي ememoryFileSyالجذعية bحقن**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Use من Google Draco (.drc) ptions ave ptions**
The C# رمز أدناه يوضح كيفية تعيين خيارات الحفظ قبل توفير نموذج 3D إلى تنسيق DRC.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Use من RVM ptions ave ptions**
The C# رمز أدناه يوضح كيفية تعيين خيارات الحفظ قبل توفير نموذج 3D إلى تنسيق RVM.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
