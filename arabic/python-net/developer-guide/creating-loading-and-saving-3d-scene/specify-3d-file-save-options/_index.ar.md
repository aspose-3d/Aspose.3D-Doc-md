---
title: Specify 3D ile ile ile ave ptions
type: docs
weight: 40
url: /ar/python-net/specify-3d-file-save-options/
description: Tهنا العديد من طريقة cencene. cenave الزائدة التي تقبل كائن ptions aveO. Each حفظ تنسيق لديه فئة المقابلة التي تحمل خيارات حفظ لهذا تنسيق حفظ.
---
## **3D ptions ile ptions ave ptions**
Tهنا العديد من [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) طريقة الأحمال الزائدة التي تقبل كائن `SaveOptions`. Tيجب أن يكون كائن من فئة مشتقة من فئة `SaveOptions`. Each حفظ تنسيق لديه فئة المقابلة التي تحمل خيارات حفظ لهذا تنسيق حفظ ، على سبيل المثال ، هناك `ColladaSaveOptions` لتنسيق حفظ `FileFormat.Collada`.
### **Use من Collada ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق Collada.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Use من Discreet3DS ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Use من FBX ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

يعرض `FBXSaveOptions` أيضًا خاصية `enable_compression` التي يمكن استخدامها لضغط البيانات الثنائية الكبيرة في ملف FBX. قيمة Default لهذه الخاصية صحيحة. Below رمز قنص يشرح كيف يمكنك العمل مع هذه الخاصية مع توفير مشهد.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Use من ptions bj ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق bj O.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Use من STL ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Use من U3D ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Use من glTF ptions ave ptions**
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 



Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق glTF.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **PrettyPrint in glTF ptions ave ptions**
You يمكن أيضا استخدام خاصية rerettyPrint من GLclass class avaveOفئة الوصفات لطباعة human understandunderstandالإنسان. Tانه رمز أدناه يظهر كيفية استخدام هذه الوظيفة.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Cies ave epepencies من 3D cencene في cenial ile ile yالجذعية**
قد تتطلب opers evelحفظ جميع اعتمادات المشهد 3D في نظام الملفات الحقيقي. Tيا يمكن تحديد مسار الدليل المحلي ، حفظ في الكائن MemoryFileSyالجذعية أو ببساطة تجاهل التبعيات. يتم إضافة property he ilileSyالجذعية الملكية في جميع الطبقات خيار حفظ.
#### **Discard aving aving المواد iles iles**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Cies ave epفي Lثماني D**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **Cies افي epependenفي ememoryFileSyالجذعية bحقن**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Use من Google Draco (.drc) ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل توفير نموذج 3D إلى تنسيق DRC.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Use من RVM ptions ave ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات الحفظ قبل توفير نموذج 3D إلى تنسيق RVM.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
