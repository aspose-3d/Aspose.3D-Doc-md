---
title: العمل بصيغة VRML
type: docs
weight: 120
url: /ar/python-net/working-with-vrml-format/
description: يسمح Aspose.3D for Python via .NET بالعمل مع الإصدار 1.0 VRML. تمت إضافة تنسيق ملف VRML إلى فئة تنسيق الملفات. Aspose. يستطيع 3D اكتشاف التنسيق تلقائيًا ، لذلك يتم تجاهل تنسيق الملف عادةً في طريقة مفتوحة. يوضح مقتطف الشفرة التالي كيفية فتح تنسيق ملف VRML.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.4 أو أكبر.

{{% /alert %}} 
#  **افتح تنسيق ملف VRML**
يسمح Aspose.3D for Python via .NET بالعمل مع الإصدار 1.0 VRML. تمت إضافة تنسيق ملف `VRML` إلى فئة `FileFormat`. Aspose. يستطيع 3D اكتشاف التنسيق تلقائيًا ، لذلك يتم تجاهل `FileFormat` عادةً في طريقة `open`. يوضح مقتطف الشفرة التالي كيفية فتح تنسيق ملف VRML.

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
