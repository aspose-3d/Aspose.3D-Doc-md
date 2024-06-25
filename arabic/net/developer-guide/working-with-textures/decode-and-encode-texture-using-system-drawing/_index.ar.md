---
title: فك ترميز النسيج باستخدام نظام. رسم
type: docs
weight: 7
url: /ar/net/decode-and-encode-texture-using-system-drawing
description: فك شفرة الملمس من ملفات الصور باستخدام System. Draving
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يستخدم المطورون أداة تشفير وفك تشفير الصور الخارجية لتحميل القوام أو حفظ القوام في تنسيقات صور مختلفة.

{{% /alert %}}

##  **تنفيذ الترميز الملمس باستخدام System.Drawing**

استخدم الفئة التالية لتحديد مشفرات النسيج وفك تشفيره:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SystemDrawing.cs" >}}


##  **سجلها في Aspose.3D**

الآن دعنا نسجله في Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


عند تسجيل برنامج الترميز هذا ، يمكن استخدام جميع تنسيقات الصور المدعومة من System. Draking في TextureData.Save.

