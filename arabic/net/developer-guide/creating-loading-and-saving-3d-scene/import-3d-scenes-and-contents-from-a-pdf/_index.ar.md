---
title: استورد 3D مشاهد ومحتويات من PDF بـ C#
linktitle: استيراد 3D مشاهد ومحتويات من PDF
type: docs
weight: 50
url: /ar/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: فئة المشهد لـ Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين استخراج 3D مشاهد ومحتويات من ملف PDF.
---
{{% alert color="primary" %}}

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين استخراج 3D مشاهد ومحتويات من ملف PDF.

{{% /alert %}}
##  **مشهد مفتوح من كلمة مرور محمية PDF**
تسمح طريقة `Open` لفئة `Scene` بتحميل مشهد 3D من ملف إدخال PDF. يمكن للمطورين أيضًا تطبيق كلمة المرور على ملفات pdf المحمية باستخدام فئة [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) كما هو موضح في مثال رمز C# هذا:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **استخراج جميع محتويات 3D الخام من PDF**
تسمح طريقة الاستخراج لفئة [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) باستخراج محتويات 3D من ملف PDF. يمكن للمطورين تكرار المحتويات وحفظها في الملفات المنعزلة كما هو موضح في مثال رمز C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **استخرج جميع مشاهد 3D وحفظها في تنسيقات 3D المدعومة**
The `ExtractScene` method of the `PdfFormat` class allows to extract 3D scenes from a PDF file. Developers may iterate through the scenes, and save them in the supported 3D file formats as shown in this C# code example:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

جميع تنسيقات الملفات المدعومة 3D مدرجة في صفحة [Roرودوكت Oفيرفيو](/3d/ar/net/product-overview/).

{{% /alert %}}
