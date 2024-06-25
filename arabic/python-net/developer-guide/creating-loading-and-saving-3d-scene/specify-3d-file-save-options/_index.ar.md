---
title: تحديد خيارات حفظ ملف 3D
type: docs
weight: 40
url: /ar/python-net/specify-3d-file-save-options/
description: Tهنا العديد من طريقة cencene. cenave الزائدة التي تقبل كائن ptions aveO. Each حفظ تنسيق لديه فئة المقابلة التي تحمل خيارات حفظ لهذا تنسيق حفظ.
---
##  **خيارات حفظ الملفات 3D**
هناك العديد من الأحمال الزائدة لطريقة [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) التي تقبل كائن `SaveOptions`. يجب أن يكون هذا موضوعًا لفئة مشتقة من فئة `SaveOptions`. يحتوي كل تنسيق حفظ على فئة مناظرة تحتوي على خيارات حفظ لتنسيق الحفظ هذا ، على سبيل المثال ، هناك `ColladaSaveOptions` لتنسيق الحفظ `FileFormat.Collada`.
###  **استخدام خيارات توفير Collada**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق Collada.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
###  **استخدام خيارات توفير Discreet3DS**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
###  **استخدام خيارات توفير FBX**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

يعرض `FBXSaveOptions` أيضًا خاصية `enable_compression` التي يمكن استخدامها لضغط بيانات ثنائية كبيرة في ملف FBX. القيمة الافتراضية لهذه الخاصية صحيحة. يشرح مقتطف الكود أدناه كيف يمكنك العمل مع هذه الخاصية أثناء حفظ المشهد.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
###  **Use من ptions bj ptions ave ptions**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D بتنسيق Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
###  **استخدام خيارات توفير STL**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ ملف 3D إلى تنسيق STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
###  **استخدام خيارات توفير U3D**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
###  **استخدام خيارات توفير glTF**
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 



يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ مستند إلى تنسيق glTF.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
###  **PrettyPrint في glTF خيارات توفير**
You يمكن أيضا استخدام خاصية rerettyPrint من GLclass class avaveOفئة الوصفات لطباعة human understandunderstandالإنسان. Tانه رمز أدناه يظهر كيفية استخدام هذه الوظيفة.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
###  **احفظ تبعيات مشهد 3D في نظام الملفات الحقيقي**
قد يحتاج المطورون إلى حفظ جميع تبعيات المشهد 3D في نظام الملفات الحقيقي. يمكنهم تحديد مسار دليل محلي ، أو حفظ كائن نظام الذاكرة أو ببساطة تجاهل التبعيات. تتم إضافة خاصية نظام الملفات في جميع فئات خيارات الحفظ.
####  **Discard aving aving المواد iles iles**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
####  **Cies ave epفي Lثماني D**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
####  **Cies افي epependenفي ememoryFileSyالجذعية bحقن**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
###  **استخدام خيارات التوفير بقيمة Google Draco (.drc)**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ نموذج 3D إلى تنسيق DRC.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
###  **استخدام خيارات توفير RVM**
يوضح الرمز أدناه كيفية تعيين خيارات الحفظ قبل حفظ نموذج 3D إلى تنسيق RVM.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
