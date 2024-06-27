---
title: فك وترميز الملمس باستخدام SkiaSharp
type: docs
weight: 9
url: /ar/net/decode-and-encode-texture-using-skiasharp
description: فك شفرة الملمس من ملفات الصور باستخدام SkiaSharp
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يستخدم المطورون أداة تشفير وفك تشفير الصور الخارجية لتحميل القوام أو حفظ القوام في تنسيقات صور مختلفة.

{{% /alert %}}


##  **استخدم الرمز التالي لتحديد ترميز نسيج من SkiaSharp**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TextureCodec-SkiaSharp.cs" >}}



##  **سجلها في Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


عند تسجيل برنامج الترميز هذا ، يمكن استخدام جميع تنسيقات الصور المدعومة من SkiaSharp في TextureData.Save.





