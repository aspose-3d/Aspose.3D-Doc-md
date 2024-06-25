---
title: إنشاء وقراءة مشهد 3D موجود
type: docs
weight: 10
url: /ar/net/create-and-read-an-existing-3d-scene/
description: Aspose. يدعم 3D API إنشاء مشاهد 3D جديدة من نقطة الصفر ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل مشهد 3D موجود لأغراض التعديل أو الإضافة أو المعالجة.
---
##  **Oفيرفيو**
توضح المقالة الموضوعات التالية باستخدام مكتبة التلاعب بتنسيقات الملفات C# 3D.
- إنشاء مشهد 3D فارغ بـ C# من الصفر
- قراءة أو تحميل مشهد 3D الحالي بـ C#
- احفظ مشهد 3D بتنسيقات 3D المدعومة باستخدام C#
- العمل مع خصائص مشهد 3D في C#

##  **قم بإنشاء مشهد 3D فارغ ووفر في تنسيقات الملفات 3D المدعومة**
Aspose. يدعم 3D API إنشاء مشاهد 3D جديدة من نقطة الصفر ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل مشهد 3D موجود لأغراض التعديل أو الإضافة أو المعالجة.

###  **إنشاء مستند مشهد 3D**
يرجى اتباع هذه الخطوات في C# لإنشاء مستند مشهد 3D باستخدام Aspose.3D APIs:

1. أنشئ مثيل لفئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) التي تمثل مستند مشهد 3D.
1. قم بإنشاء مستند مشهد 3D عن طريق استدعاء طريقة [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) لكائن فئة المشهد.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

##  **قراءة مشهد 3D**
باستخدام Aspose.3D API ، يمكن للمطورين تحميل جميع مستندات 3D المدعومة. تسمح المنشئات المتاحة لفئة `Scene` بذلك وتقبل سلسلة مسار ملف صالحة. تنسيقات الملفات المقروءة المدعومة هي كما يلي:

1. FBX 7.5 (ASCII ، ثنائي)
1. FBX 7.4 (ASCII ، ثنائي)
1. FBX 7.3 (ASCII ، ثنائي)
1. FBX 7.2 (ASCII ، ثنائي)
1. FBX 6.1 (ASCII ، ثنائي)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, Binary)
1. مايا (أسكي ، ثنائي)
1. OpenUSD (USD ، USDZ)
1. خلاط
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCI I ، inary inary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

تكتشف منشئات فئة `Scene` تنسيق المستند 3D داخليًا.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

##  **العمل مع خصائص المشهد 3D**
Aspose.3D API يتيح لك قراءة خصائص المشهد 3D باستخدام عقد الطفل للمشهد. توضح عينة رمز C# التالية استخدام هذه الميزة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
