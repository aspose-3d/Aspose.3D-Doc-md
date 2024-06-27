---
title: إنشاء وقراءة مشهد 3D موجود
type: docs
weight: 10
url: /ar/python-net/create-and-read-an-existing-3d-scene/
description: Aspose. يدعم 3D API إنشاء مشاهد 3D جديدة من نقطة الصفر ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل مشهد 3D موجود لأغراض التعديل أو الإضافة أو المعالجة.
---
##  **قم بإنشاء مشهد 3D فارغ ووفر في تنسيقات الملفات 3D المدعومة**
Aspose. يدعم 3D API إنشاء مشاهد 3D جديدة من نقطة الصفر ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل مشهد 3D موجود لأغراض التعديل أو الإضافة أو المعالجة.
###  **إنشاء مستند مشهد 3D**
يرجى اتباع هذه الخطوات لإنشاء مستند مشهد 3D باستخدام Aspose.3D APIs:

1. أنشئ مثيل لفئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) التي تمثل مستند مشهد 3D.
1. قم بإنشاء مستند مشهد 3D عن طريق استدعاء طريقة [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) لكائن فئة المشهد.
####  **إنشاء مستند مشهد 3D: عينات برمجة**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
##  **قراءة مشهد 3D**
باستخدام Aspose.3D API ، يمكن للمطورين تحميل جميع مستندات 3D المدعومة. المنشئات المتاحة من**مشهد**تسمح الفئة بذلك وتقبل سلسلة مسار ملف صالحة. Tكان يدعم تنسيقات الملفات القابلة للقراءة هي كما يلي:

1. FBX 7.7 (ASCII ، ثنائي)
1. FBX 7.6 (ASCII, Binary)
1. FBX 7.5 (ASCII ، ثنائي)
1. FBX 7.4 (ASCII ، ثنائي)
1. FBX 7.3 (ASCII ، ثنائي)
1. FBX 7.2 (ASCII ، ثنائي)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCI I ، inary inary)
1. XYZ
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE
1. USDZ
1. USD

تكتشف منشئات فئة `Scene` تنسيق المستند 3D داخليًا.
###  **قراءة مشهد 3D: عينات برمجة**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
