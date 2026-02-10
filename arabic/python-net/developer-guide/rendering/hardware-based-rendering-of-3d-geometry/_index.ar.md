---
title: تقديم قائم على الأجهزة بقيمة 3D هندسة
type: docs
weight: 30
url: /ar/python-net/hardware-based-rendering-of-3d-geometry/
description: Using Aspose.3D for Python via .NET API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. 
---
{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. In this article, we focus on hardware-based rendering using [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **إنشاء الأجهزة وتقديم هندسة 3D**
مطلوب تقديم شكل هندسي 3D ، تظليل ، مخازن وحالة تقديم. لا يمكن لأي منهم العمل دون الآخر.

- **Uuffers**-قوائم riangle Tهي مثلثات فردية محددة في صفيف يشار إليها أحيانا باسم المخزن المؤقت. In قائمة مثلث ، يتم تحديد كل مثلث بشكل فردي. يمكن مشاركة oinللمثلث باستخدام مؤشرات لتقليل كمية البيانات التي يجب تمريرها إلى أجهزة الرسومات.
- **Sهادرز**-It يحدد كيفية تحويل المثلثات من الفضاء العالمي إلى مساحة الشاشة وحساب لون بكسل النهائي في الجانب GPU
- **Render تيتس**-يوفر It المعلمات ل GPraraالمثلثات إلى بكسل.

{{% alert color="primary" %}}

قمنا بإعداد مشروع تجريبي. يرجى الرجوع إلى [هذا تحميل URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

لغة تظليل OpenGL (GLSL) هي لغة تظليل قياسية عالية المستوى لرسومات OpenGL API. هناك ثلاثة أنواع من التظليل شائعة الاستخدام: تظليل الرأس ، تظليل الشظية ، تظليل الهندسة.

فئة [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) تخبر المستعرض ، رمز المصدر هو لغة تظليل OpenGL ، ويمكن تجميعها إلى فئة [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). تحدد فئة [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) المتغيرات المستخدمة في التظليل. تُستخدم فئة `VariableSemantic` لتحديد الدلالية لمتغير التظليل ، Aspose. سيقوم المستعرض 3D بإعداد قيم متغير التظليل تلقائيًا بناءً على الدلالات.
###  **Pروغرامينغ ple وافرة ل Shader**
هذا المثال رمز تهيئة العارضين وتظليل للشبكة. يمكنك تنزيل مشروع العمل الكامل لهذا المثال من [هنا](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
###  **Pروغرامينغ ple وافرة ل Bأوفر و Render تايت**
Tله رمز المثال يبدأ المخزن المؤقت وتقديم الدولة للشبكة.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
