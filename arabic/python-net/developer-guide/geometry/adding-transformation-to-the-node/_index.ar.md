---
title: Aدينغ رانسفورميشن إلى oode
type: docs
weight: 30
url: /ar/python-net/adding-transformation-to-the-node/
description: تُستخدم TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، قدمنا تحويل فئة للوصول إليها بـ Aspose.3D.
---
{{% alert color="primary" %}}

يعرض Aspose.3D for Python via .NET تدوير الكائنات في مساحة 3D. هناك ثلاث طرق لتحديد دوران الكائن في مساحة 3D وزوايا Euler و Quaternion والمصفوفة المخصصة ، وكلها مدعومة بفئة [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

تُستخدم TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، وقدمنا فئة `Transform` للوصول إليها بـ Aspose.3D. وتشمل التحولات في التخلف:

- تصنيف:
- Calالترسبات
- Rأوتيشن
- Hear سماع رسم الخرائط
- رسم الخرائط

{{% alert color="primary" %}}

كائن الفئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة `Mesh` كما روى هناك](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Rotate بواسطة Quaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
##  **Rotate بواسطة Euler ngngles**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
##  **Custom ranransformation atatrix**
We يمكن أيضا استخدام Matrix مباشرة:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
