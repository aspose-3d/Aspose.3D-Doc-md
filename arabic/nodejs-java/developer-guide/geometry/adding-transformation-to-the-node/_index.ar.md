---
title: إضافة تحويل إلى العقدة
type: docs
weight: 10
url: "/ar/nodejs-java/adding-transformation-to-the-node/"
description: "يوفر Aspose.3D لـ Node.js عبر Java API دعمًا لتدوير الكائنات في الفضاء ثلاثي الأبعاد. هناك ثلاث طرق لتحديد دوران الكائن في الفضاء ثلاثي الأبعاد، وهي الزوايا أويلر، والكواترنيون، والمصفوفة المخصصة، ويدعمها جميعًا فئة Transform."
---

{{% alert color="primary" %}}

Aspose.3D for Node.js via Java API لديه دعم لتدوير الكائنات في الفضاء ثلاثي الأبعاد. هناك ثلاث طرق لتحديد دوران الكائن في الفضاء ثلاثي الأبعاد، زوايا أويلر، كواتيرنيون ومصفوفة مخصصة، جميعها مدعومة بواسطة الفئة `Transform`.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) هي الأكثر استخدامًا في السيناريو ثلاثي الأبعاد، لقد قدمنا فئة `Transform` للوصول إلى هذه التحويلات الخطية في Aspose.3D. تتضمن التحويلات الخطية:

- Translation (الترجمة)
- Scaling (القياس)
- Rotation (الدوران)
- Shear mapping (رسم الخرائط القص)
- Squeeze mapping (رسم الخرائط الضغط)

## **Rotate by Euler Angles**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize scene object
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Euler angles
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Set translation
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Save
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Custom Transformation Matrix**
يمكننا أيضًا استخدام Matrix مباشرة:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize scene object
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Set custom translation matrix
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Save
scene.save("TransformationToNode.obj");

{{< /highlight >}}
