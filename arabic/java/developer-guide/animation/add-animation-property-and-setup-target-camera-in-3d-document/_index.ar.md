---
title: إضافة خاصية الرسوم المتحركة وإعداد الكاميرا المستهدفة في مستند 3D
type: docs
weight: 10
url: /ar/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java يدعم عرض مشهد متحرك. تشرح هذه المقالة المتطلبات الأساسية لنقل كائن ما.
---
##  **إضافة خاصية الرسوم المتحركة في مستند 3D**
Aspose.3D for Java يدعم عرض مشهد متحرك. تشرح هذه المقالة المتطلبات الأساسية لنقل كائن ما.
###  **Sition ove sition sition sition**
{{% alert color="primary" %}}

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) ويجب أن نتحرك خاصية الترجمة المحلية للعقدة أيضًا: [Aدينغ رانسوفورميشن إلى oode](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API, animation instance is actually key-frame animation that animates on properties. In order animate properties, you need a `CurveMapping` instance which maps components of a property to different curves, for example, a `Vector3` property can have 3 components `X`/`Y`/`Z`, which will set up three channels in `CurveMapping`, every channel can have a set of `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **إعداد الكاميرا المستهدفة في ملف 3D**
Aspose.3D for Java عروض لإعداد الكاميرا المستهدفة في ملف 3D. في بعض تنسيقات الملفات ، يدعم الضوء/الكاميرا الهدف ، مما يسمح للضوء/الكاميرا دائمًا بمواجهة عقدة محددة ، وهذا مفيد في الرسوم المتحركة.

{{% alert color="primary" %}}

The `Scene`, `Camera`, `Node` and `Transform` classes are being used in the code. in order to save a `Scene`, `Scene.save` method is being used, it accepts a file name with complete path and `FileFormat` parameter.

{{% /alert %}}

في المثال أدناه ، تم إعداد الهدف والكاميرا في ملف 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
