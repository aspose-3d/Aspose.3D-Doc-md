---
title: أول تطبيق Aspose لك. 3D
type: docs
weight: 30
url: /ar/net/your-first-aspose-3d-application/
description: قم بإنشاء أول ملف 3d الخاص بك وتحريره وحفظه في أي تنسيقات مدعومة باستخدام Aspose.3D for .NET لتجربة بساطته وقوته بسعر C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

يشرح هذا البرنامج التعليمي كيفية إنشاء تطبيقك الأول باستخدام Aspose.3D البسيط API. يُنشئ هذا التطبيق البسيط ملفًا ثلاثي الأبعاد في مشهد 3D محدد.

{{% /alert %}}

##  **كيف يتم إنشاء التطبيق**

تنشئ الخطوات أدناه التطبيق باستخدام Aspose.3D API:

1. أنشئ مثيل لفئة [مشهد](https://reference.aspose.com/3d/net/aspose.threed/scene/).
1. إذا كان لديك ترخيص ، فعندئذ [تطبيق عليه](/3d/ar/net/licensing/).
إذا كنت تستخدم إصدار التقييم ، فتخطي خطوط التعليمات البرمجية ذات الصلة بالترخيص.
1. أنشئ ملف 3D جديد ، أو افتح ملف 3D موجود.
1. الوصول إلى محتويات المشهد في ملف 3D.
1. إنشاء ملف 3D المعدل.

يتم توضيح تنفيذ الخطوات المذكورة أعلاه في الأمثلة أدناه.

###  **كيفية إنشاء مستند مشهد جديد**

يُنشئ المثال التالي ملف مشهد 3D جديد من الصفر. أولاً ، أنشئ مشهد 3D ثم احفظ الملف بتنسيق FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

###  **كيفية فتح ملف موجود**

يفتح المثال التالي ملف قالب 3D موجود يسمى "document.fbx" ثم يحفظ مشهد أو مستند 3D في تدفق بتنسيقات مختلفة مدعومة من 3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
