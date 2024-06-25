---
title: حدد خيارات حفظ ملف 3D بـ C#
linktitle: تحديد خيارات حفظ ملف 3D
type: docs
weight: 40
url: /ar/net/specify-3d-file-save-options/
description: Tهنا العديد من طريقة cencene. cenave الزائدة التي تقبل كائن ptions aveO. Each حفظ تنسيق لديه فئة المقابلة التي تحمل خيارات حفظ لهذا تنسيق حفظ.
---
##  **Oفيرفيو**

توضح هذه المقالة كيف يمكنك حفظ ملفات 3D في تنسيقات مختلفة [بعد تحميلها في كائن Scene](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) باستخدام C#. من خلال التحميل والحفظ ، يمكنك تنفيذ عدد من التحويلات المختلفة على سبيل المثال

- تحويل FBX إلى X بـ C#
- تحويل GLTF إلى OBJ في C#
- تحويل OBJ إلى X بـ C#
- تحويل STL إلى OBJ في C#
- تحويل RVM إلى 3DS في C#

##  **خيارات حفظ الملفات 3D**
هناك العديد من الأحمال الزائدة لطريقة [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) التي تقبل كائن SaveOptions. يجب أن يكون هذا موضوعًا لفئة مشتقة من فئة `SaveOptions`. يحتوي كل تنسيق حفظ على فئة مناظرة تحتوي على خيارات حفظ لتنسيق الحفظ هذا ، على سبيل المثال ، هناك `ColladaSaveOptions` لتنسيق حفظ `FileFormat.Collada`.
###  **استخدام خيارات توفير Collada**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق Collada.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
###  **استخدام خيارات توفير Discreet3DS**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق 3DS غير ظاهر.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
###  **استخدام خيارات توفير FBX**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

يعرض `FBXSaveOptions` أيضًا خاصية `EnableCompression` التي يمكن استخدامها لضغط بيانات ثنائية كبيرة في ملف FBX. القيمة الافتراضية لهذه الخاصية صحيحة. يشرح مقتطف الكود أدناه كيف يمكنك العمل مع هذه الخاصية أثناء حفظ المشهد.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
###  **Use من ptions bj ptions ave ptions**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D بتنسيق Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
###  **استخدام خيارات توفير STL**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
###  **استخدام خيارات توفير U3D**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
###  **استخدام خيارات توفير glTF**
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 



يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق glTF.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
###  **PrettyPrint في glTF خيارات توفير**
You يمكن أيضا استخدام خاصية rerettyPrint من GLclass class avaveOفئة الوصفات لطباعة human understandunderstandالإنسان. Tانه رمز أدناه يظهر كيفية استخدام هذه الوظيفة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
###  **احفظ تبعيات مشهد 3D في نظام الملفات الحقيقي**
قد يحتاج المطورون إلى حفظ جميع تبعيات المشهد 3D في نظام الملفات الحقيقي. يمكنهم تحديد مسار دليل محلي ، أو حفظ كائن `MemoryFileSystem` أو ببساطة تجاهل التبعيات. تمت إضافة خاصية `FileSystem` في جميع فئات خيارات الحفظ.
####  **Discard aving aving المواد iles iles**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
####  **Cies ave epفي Lثماني D**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
####  **Cies افي epependenفي ememoryFileSyالجذعية bحقن**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
###  **استخدام خيارات التوفير بقيمة Google Draco (.drc)**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ نموذج 3D إلى تنسيق DRC.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
###  **استخدام خيارات توفير RVM**
يوضح رمز C# أدناه كيفية تعيين خيارات الحفظ قبل حفظ نموذج 3D إلى تنسيق RVM.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
