---
title: وفِّر مشهد 3D في PDF
type: docs
weight: 60
url: /ar/python-net/save-a-3d-scene-in-the-pdf/
description: فئة المشهد لـ Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين بناء مشهد 3D عن طريق إضافة الكاميرا والضوء والمضلعات ومختلف الكيانات الأخرى. يمكنهم أيضًا الآن حفظ مشهد 3D بتنسيق الملف PDF.
---
{{% alert color="primary" %}} 

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مشهد 3D. يمكن للمطورين بناء مشهد 3D بإضافة الكاميرا والضوء والمضلعات ومختلف الكيانات الأخرى. كما يمكنهم الآن حفظ مشهد 3D بتنسيق الملف PDF.

{{% /alert %}} {{% alert color="primary" %}} 

يكتب Aspose.3D for Python via .NET مباشرةً المعلومات حول API ورقم الإصدار في مستندات الإخراج. على سبيل المثال ، عند تحويل السحب إلى PDF ، يقوم Aspose.3D for Python via .NET بملء حقل `Application` بقيمة Aspose. حقل 3D "و `PDF Producer` مع القيمة ، هـ. g Aspose.3D 17.9".

يرجى ملاحظة أنه لا يمكنك طلب Aspose. رسم بياني لـ Python via .NET API لتغيير هذه المعلومات أو إزالتها من مستندات الإخراج.

{{% /alert %}} 
##  **Create a 3D PDF with a Cylinder, and Rendered in Shaded Illustration Mode with CAD Optimized Lighting**
تتيح طريقة التوفير لفئة `Scene` حفظ مشهد 3D بتنسيق PDF. يمكن للمطورين تحميل أي ملف مدعوم بمبلغ 3D أو إنشاء مشهد 3D جديد ، ويمكنهم توفير مشهد 3D بتنسيق PDF كما هو موضح في مثال الرمز هذا:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Cylinder
from aspose.threed.shading import PhongMaterial
from aspose.threed.formats import PdfSaveOptions, PdfLightingScheme, PdfRenderMode
# Create a new scene
scene = Scene()
# Create a cylinder child node
cylinder = scene.root_node.create_child_node("cylinder", Cylinder())
cylinder.material = PhongMaterial()
# Set rendering mode and lighting scheme
opt = PdfSaveOptions()
opt.lighting_scheme = PdfLightingScheme.CAD
opt.render_mode = PdfRenderMode.SHADED_ILLUSTRATION
# Save in the PDF format
scene.save("output_out.pdf", opt)

{{< /highlight >}}
