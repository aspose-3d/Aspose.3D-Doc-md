---
title: فك تشفير الملمس باستخدام ImageSharp
type: docs
weight: 11
url: /ar/net/decode-and-encode-texture-using-imagesharp
description: فك شفرة الملمس من ملفات الصور باستخدام ImageSharp
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يستخدم المطورون أداة تشفير وفك تشفير الصور الخارجية لتحميل القوام أو حفظ القوام في تنسيقات صور مختلفة.

{{% /alert %}}

##  **تنفيذ الترميز الملمس باستخدام ImageSharp**

استخدم الفئة التالية لتحديد مشفرات النسيج وفك تشفيره:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-ImageSharpCodec.cs" >}}


##  **سجلها في Aspose.3D**

الآن دعنا نسجله في Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{< /highlight >}}


عند تسجيل برنامج الترميز هذا ، يمكن استخدام جميع تنسيقات الصور المدعومة من ImageSharp في TextureData.Save.

