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

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import PdfLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a new scene
scene = Scene()
options = PdfLoadOptions()
options.password = "password".encode("utf-8")
#  Use loading options and apply password
opt = options
#  Open scene
scene.open("data-dir"  + "House_Design.pdf", opt)

{{< /highlight >}}
##  **استخراج جميع محتويات 3D الخام من PDF**
تتيح طريقة `extract` لفئة [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) استخراج محتويات 3D من ملف PDF. يمكن للمطورين تكرار المحتويات وحفظها في ملفات منفصلة كما هو موضح في مثال الكود هذا:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
password = None
#  Extract 3D contents
contents = FileFormat.PDF.extract("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the contents and in separate 3D files
for content in contents:
    fileName = "3d-"  + str(i)
    i = i + 1
    with open(fileName, "wb") as f:
        f.write(content)

{{< /highlight >}}
##  **استخرج جميع مشاهد 3D وحفظها في تنسيقات 3D المدعومة**
تتيح طريقة `extract_scene` لفئة `PdfFormat` استخراج مشاهد 3D من ملف PDF. يمكن للمطورين تكرار المشاهد وحفظها في تنسيقات الملفات المدعومة 3D كما هو موضح في مثال الرمز هذا:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
password = None
scenes = FileFormat.PDF.extract_scene("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the scenes and save in 3D files
for scene in scenes:
    fileName = "3d-"  + str(i) + ".fbx"
    i = i + 1
    scene.save("out"  + fileName, FileFormat.FBX7400ASCII)

{{< /highlight >}}

{{% alert color="primary" %}}

جميع تنسيقات الملفات المدعومة 3D مدرجة في صفحة [Roرودوكت Oفيرفيو](/3d/ar/python-net/product-overview/).

{{% /alert %}}
