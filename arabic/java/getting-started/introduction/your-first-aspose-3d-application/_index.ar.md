---
title: أول تطبيق Aspose لك. 3D
type: docs
weight: 30
url: /ar/java/your-first-aspose-3d-application/
description: قم بإنشاء أول ملف 3d الخاص بك وتحريره وحفظه في أي تنسيقات مدعومة باستخدام Aspose.3D for Java لتجربة بساطته وقوته بسعر Java.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---
{{% alert color="primary" %}}

يشرح هذا البرنامج التعليمي كيفية إنشاء تطبيقك الأول باستخدام Aspose.3D البسيط API. يُنشئ هذا التطبيق البسيط ملفًا ثلاثي الأبعاد في مشهد 3D محدد.

{{% /alert %}}

##  **كيف يتم إنشاء التطبيق**

تنشئ الخطوات أدناه التطبيق باستخدام Aspose.3D API:

1. أنشئ مثيل لفئة [مشهد](https://reference.aspose.com/3d/java/com.aspose.threed/scene/).
1. إذا كان لديك ترخيص ، فعندئذ [تطبيق عليه](/3d/ar/java/licensing/).
إذا كنت تستخدم إصدار التقييم ، فتخطي خطوط التعليمات البرمجية ذات الصلة بالترخيص.
1. أنشئ ملف 3D جديد ، أو افتح ملف 3D موجود.
1. الوصول إلى محتويات المشهد في ملف 3D.
1. إنشاء ملف 3D المعدل.

يتم توضيح تنفيذ الخطوات المذكورة أعلاه في الأمثلة أدناه.

###  **كيفية إنشاء مستند مشهد جديد**

يُنشئ المثال التالي ملف مشهد 3D جديد من الصفر. أولاً ، أنشئ مشهد 3D ثم احفظ الملف بتنسيق FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}

###  **كيفية فتح ملف موجود**

يفتح المثال التالي ملف قالب 3D موجود يسمى "document.fbx" ثم يحفظ مشهد أو مستند 3D في تدفق بتنسيقات مختلفة مدعومة من 3D.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3D document into Aspose.3D
Scene scene = new Scene();
// Open an existing 3D scene
scene.open(MyDir + "document.fbx");
// Save Scene to a stream
try (MemoryStream dstStream = new MemoryStream()) {
    scene.save(dstStream, FileFormat.FBX7500ASCII);
}
// Save Scene to a local path
scene.save(MyDir + "output_out.fbx", FileFormat.FBX7500ASCII);
{{< /highlight >}}
