---
title: Hardware ased ased من 3D omeeometry
type: docs
weight: 30
url: /ar/net/hardware-based-rendering-of-3d-geometry/
description: Using Aspose.3D for .NET API ، يمكن للمطورين برمجة GPU (وحدة معالجة الرسومات) وإعداد أجهزة الرسومات لتقديم الهندسة 3D بدلا من خط أنابيب وظيفة ثابتة.
---
{{% alert color="primary" %}}

Uالغناء[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API ، يمكن للمطورين برمجة GPU (وحدة معالجة الرسومات) وإعداد أجهزة الرسومات لتقديم الهندسة 3D بدلا من خط أنابيب وظيفة ثابتة. In هذه المقالة ، ونحن نركز على تقديم القائمة على الأجهزة باستخدام[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Assx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). اسبكس) و[Vأولكان](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
## **Create ardardware و ender ender a 3D omeeometry**
To تقديم الهندسة 3D ، مطلوب شادر ، المخازن المؤقتة وتقديم الدولة. Nواحد منهم يمكن أن تعمل دون بعضها البعض.

- **Uuffers**-قوائم riangle Tهي مثلثات فردية محددة في صفيف يشار إليها أحيانا باسم المخزن المؤقت. In قائمة مثلث ، يتم تحديد كل مثلث بشكل فردي. يمكن مشاركة oinللمثلث باستخدام مؤشرات لتقليل كمية البيانات التي يجب تمريرها إلى أجهزة الرسومات.
- **Sهادرز**-It يحدد كيفية تحويل المثلثات من الفضاء العالمي إلى مساحة الشاشة وحساب لون بكسل النهائي في الجانب GPU
- **Render تيتس**-يوفر It المعلمات ل GPraraالمثلثات إلى بكسل.

{{% alert color="primary" %}}

وقد أعدت We مشروع تجريبي. Lease الإيجار تشير إلى[هذا تحميل URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

The OpenGL Shading anganguage (GLSL) هي لغة التظليل عالية المستوى القياسية للرسومات OpenGL API. The `InitRenderer` طريقة في `AssetBrowser/Controls/RenderView.cs` ملف تحت التطبيق التجريبي (الاسم: AssetBrowser) يوضح الاستخدام البسيط GLL باستخدام Aspose.3D API. Tهنا ثلاثة أنواع شادر تستخدم عادة: Vertex hadهادرز ، hadراغمنت هادر و Geometry Sهادرز.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) فئة يخبر المستأجر ، رمز المصدر هو لغة التظليل OpenGL ، يمكن تجميعها إلى فئة [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). The [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) فئة يحدد المتغيرات المستخدمة في شادر. يستخدم he he `VariableSemantic` الفئة لتحديد الدلالية متغير شادر ، Aspose.3D المستأجر تلقائيا إعداد القيم المتغيرة شادر يعتمد على الدلالات.
### **Pروغرامينغ ple وافرة ل Shader**
Tله رمز المثال يبدأ المستأجر و Shader للشبكة. You يمكن تحميل مشروع العمل الكامل لهذا المثال من[هنا](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Controls-RenderView-RenderView.cs" >}}
### **Pروغرامينغ ple وافرة ل Bأوفر و Render تايت**
Tله رمز المثال يبدأ المخزن المؤقت وتقديم الدولة للشبكة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Grid-ManualEntity.cs" >}}
