---
title: تقديم مشهد 3D في صفحة الويب
type: docs
weight: 50
url: /ar/net/render-3d-scene-in-web-page/
description: باستخدام Aspose.3D for .NET ، يمكن للمطورين عرض صورة لعرض صورة واقعية لطراز 3D ، مع أو بدون الخلفية المحسنة ، والقوام ، والظلال ، وكذلك ضبط حجم الصورة.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يمكن للمطورين تحويل مشهد 3D إلى ملف USDZ ، وتصوره في صفحة الويب باستخدام Aspose.3D جهاز عرض الويب.

{{% /alert %}}

##  **احصل على عارض الويب**

يمكنك الحصول على عارض الويب من [الإصدارات](https://releases.aspose.com/3d/net/) لدينا ، هناك 4 ملفات في مجلد `web-renderer`:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat
* Aspose.3d-2.1.wasm
* Asplose3d. d.ts


##  **تحويل مشهد إلى ملف USDZ**
يدعم عرض الويب لدينا استيراد USDZ وتصديره داخل متصفح الويب ، نحتاج إلى تحويل المشهد إلى USDZ قبل تصوره في متصفح الويب ، عينة الرمز لتحويل المشهد إلى ملف USDZ:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **خدمة الملف من خلال خادم HTTP**

نظرًا لقيود المتصفح ، يجب تقديم جميع الملفات بما في ذلك مستعرض الويب وملف 3D من خلال بروتوكول HTTP/HTTPS ، يمكنك استخدام سطر أوامر python لبدء خادم http بسيط يقوم بالاستماع على المنفذ 8000:

```
python3 -m http.server
```

##  **تحميل المشهد باستخدام جافا سكريبت**

إنشاء صفحة HTML جديدة ، وتحميل عرض الويب:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Aspose.3D Web Renderer</title>
        <script src="aspose.3d-2.1.js"></script>
    <style>
        #canvas{width:600px;height:400px;}
    </style>

    </head>
    <body>
        <h1>Aspose.3D Web Renderer</h1>
        <canvas id='canvas'></canvas>
        <script>
            aspose3d({canvas : 'canvas', url : 'test.usdz'});
        </script>
    </body>
</html>
```

يمكن العثور على مزيد من المعلومات بقيمة `aspose3d` في ملف إعلان النسخة المطبوعة `aspose3d.d.ts`.
