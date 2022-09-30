---
title: Add nimnimation roroperty و tup etop ararget amamera في 3D وثيقة
type: docs
weight: 10
url: /ar/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java يدعم تقديم مشهد الرسوم المتحركة. Tمقالته يفسر المتطلبات الأساسية لنقل كائن.
---
## **Property dd nimnimation الملكية في 3D وثيقة**
Aspose.3D for Java يدعم تقديم مشهد الرسوم المتحركة. Tمقالته يفسر المتطلبات الأساسية لنقل كائن.
### **Sition ove sition sition sition**
{{% alert color="primary" %}}

Tهو `Mesh` يتم استخدام كائن فئة في التعليمات البرمجية. We يمكن[إنشاء كائن فئة Mesh كما روى هناك](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)ويجب أن تحريك خاصية الترجمة المحلية للعقدة أيضا:[Aدينغ رانسوفورميشن إلى oode](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API ، مثال الرسوم المتحركة هو في الواقع مفتاح الإطار الرسوم المتحركة التي تتحرك على الخصائص. In الطلب خصائص متحركة ، تحتاج إلى `CurveMapping` مثيل الذي خرائط مكونات خاصية إلى منحنيات مختلفة ، على سبيل المثال ، خاصية `Vector3` يمكن أن يكون لها 3 مكونات `X`/`Y`/`Z` ، والتي سيتم إعداد ثلاث قنوات في `CurveMapping` ، كل قناة يمكن أن يكون لها مجموعة من `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Tup etop Target amamera في 3D ile ile**
Aspose.3D for Java يقدم لإعداد الكاميرا المستهدفة في ملف 3D. In بعض صيغ الملفات ، الضوء/الكاميرا يدعم الهدف ، والذي يسمح للضوء/الكاميرا تواجه دائما عقدة محددة ، وهذا مفيد في الرسوم المتحركة.

{{% alert color="primary" %}}

The `Scene` ، `Camera` ، `Node` و `Transform` يتم استخدام الطبقات في الرمز. من أجل حفظ `Scene` ، يتم استخدام طريقة `Scene.save` ، فإنه يقبل اسم الملف مع مسار كامل ومعلمة `FileFormat`.

{{% /alert %}}

In أدناه المثال ، يتم إعداد الهدف والكاميرا في ملف 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
