---
title: Aدينغ رانسفورميشن إلى oode
type: docs
weight: 10
url: /ar/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API لديه دعم لتدوير الأجسام في مساحة 3D. Tهنا هي ثلاث طرق لتحديد دوران الكائن في مساحة 3D ، زوايا Euler ، uuaternion و Custom atatrix ، يتم دعم كل منهم من قبل فئة ranransform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API لديه دعم لتدوير الأجسام في مساحة 3D. Tهنا هي ثلاث طرق لتحديد دوران الكائن في مساحة 3D ، زوايا Euler ، Quaternion و Custom atatrix ، يتم دعم كل منهم من قبل فئة `Transform`.

{{% /alert %}} 

TranR (ranranslation/calالترسبات/الترسبات) هي الأكثر شيوعا في 3D السيناريو ، قدمنا فئة `Transform` للوصول إلى هذه في Aspose.3D transformffine التحولات تشمل:

- تصنيف:
- Calالترسبات
- Rأوتيشن
- Hear سماع رسم الخرائط
- رسم الخرائط

{{% alert color="primary" %}} 

Tهو `Mesh` يتم استخدام كائن فئة في التعليمات البرمجية. We يمكن[إنشاء كائن فئة Mesh كما روى هناك](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Rotate بواسطة Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Rotate بواسطة Euler ngngles**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Custom ranransformation atatrix**
We يمكن أيضا استخدام Matrix مباشرة:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
