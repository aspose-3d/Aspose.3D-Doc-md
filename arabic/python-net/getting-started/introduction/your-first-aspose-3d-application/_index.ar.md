---
title: تطبيقك الأول باستخدام Aspose.3D
type: docs
weight: 30
url: /ar/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

يشرح هذا البرنامج التعليمي كيفية إنشاء تطبيقك الأول باستخدام واجهة برمجة التطبيقات البسيطة لبرنامج Aspose.3D. يقوم هذا التطبيق البسيط بإنشاء ملف ثلاثي الأبعاد في مشهد ثلاثي الأبعاد محدد.

{{% /alert %}}

## **كيفية إنشاء التطبيق**

تقوم الخطوات التالية بإنشاء التطبيق باستخدام واجهة برمجة التطبيقات Aspose.3D:

1. قم بإنشاء نسخة من فئة [Scene](https://reference.aspose.com/3d/ar/python-net/aspose.threed/scene/).
1. إذا كنت تمتلك رخصة، فقم [باستخدامها](/3d/ar/python-net/licensing/).  
   إذا كنت تستخدم الإصدار التجريبي، فتجاوز سطور الكود المتعلقة بالرخصة.
1. قم بإنشاء ملف ثلاثي الأبعاد جديد أو فتح ملف ثلاثي الأبعاد موجود.
1. قم بالوصول إلى محتويات المشهد داخل الملف الثلاثي الأبعاد.
1. قم بإنشاء الملف الثلاثي الأبعاد المعدل.

يتم عرض تنفيذ الخطوات المذكورة أعلاه في الأمثلة التالية.

### **كيفية إنشاء مستند مشهد جديد** 

يقوم المثال التالي بإنشاء ملف مشهد ثلاثي الأبعاد جديد من البداية. أولاً قم بإنشاء مشهد ثلاثي الأبعاد ثم احفظ الملف بصيغة FBX.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)

{{< /highlight >}}

### **كيفية فتح ملف موجود**

يقوم المثال التالي بفتح ملف قالب ثلاثي الأبعاد موجود باسم "document.fbx".

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")


{{< /highlight >}}
