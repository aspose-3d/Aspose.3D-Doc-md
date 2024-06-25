---
title: استيراد 3D مشاهد ومحتويات من PDF
type: docs
weight: 50
url: /ar/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: فئة المشهد لـ Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين استخراج 3D مشاهد ومحتويات من ملف PDF.
---
{{% alert color="primary" %}}

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين استخراج 3D مشاهد ومحتويات من ملف PDF.

{{% /alert %}}
##  **مشهد مفتوح من كلمة مرور محمية PDF**
تسمح طريقة `open` لفئة `Scene` بتحميل مشهد 3D من ملف إدخال PDF. يمكن للمطورين أيضًا تطبيق كلمة المرور لأجهزة pdf المحمية باستخدام فئة [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) كما هو موضح في مثال الرمز هذا:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
##  **استخراج جميع محتويات 3D الخام من PDF**
تتيح طريقة `extract` لفئة [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) استخراج محتويات 3D من ملف PDF. يمكن للمطورين تكرار المحتويات وحفظها في ملفات منفصلة كما هو موضح في مثال الكود هذا:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
##  **استخرج جميع مشاهد 3D وحفظها في تنسيقات 3D المدعومة**
تتيح طريقة `extract_scene` لفئة `PdfFormat` استخراج مشاهد 3D من ملف PDF. يمكن للمطورين تكرار المشاهد وحفظها في تنسيقات الملفات المدعومة 3D كما هو موضح في مثال الرمز هذا:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

جميع تنسيقات الملفات المدعومة 3D مدرجة في صفحة [Roرودوكت Oفيرفيو](/3d/ar/python-net/product-overview/).

{{% /alert %}}
