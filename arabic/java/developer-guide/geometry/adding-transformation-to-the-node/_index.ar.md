---
title: Aدينغ رانسفورميشن إلى oode
type: docs
weight: 10
url: /ar/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API لديه دعم لتدوير الكائنات في مساحة 3D. هناك ثلاث طرق لتعريف دوران الكائن بمساحة 3D وزوايا Euler و Quaternion والمصفوفة المخصصة ، وكلها مدعومة بفئة التحويل.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API لديه دعم لتدوير الكائنات في مساحة 3D. هناك ثلاث طرق لتحديد دوران الكائن في مساحة 3D وزوايا Euler و Quaternion والمصفوفة المخصصة ، وكلها مدعومة بفئة `Transform`.

{{% /alert %}} 

يتم استخدام TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، وقدمنا فئة `Transform` للوصول إليها بـ Aspose. تتضمن تحويلات الأوفياء 3D ما يلي:

- تصنيف:
- Calالترسبات
- Rأوتيشن
- Hear سماع رسم الخرائط
- رسم الخرائط

{{% alert color="primary" %}} 

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Rotate بواسطة Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
##  **Rotate بواسطة Euler ngngles**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
##  **Custom ranransformation atatrix**
We يمكن أيضا استخدام Matrix مباشرة:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
