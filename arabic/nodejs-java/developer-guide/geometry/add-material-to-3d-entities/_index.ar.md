---
title: إضافة مواد إلى الكيانات ثلاثية الأبعاد
type: docs
weight: 60
url: "/ar/nodejs-java/add-material-to-3d-entities/"
description: يلعب PBR دورًا رئيسيًا في مرئيات محرك الألعاب، بفضل تصويره الفعال والواقعي لتفاعلات الضوء والسطح من خلال التوهين وتشتت الضوء المنعكس. يمكن للمطورين استخدام واجهة برمجة تطبيقات Aspose.3D لتطبيق مادة PBR على الكائنات ثلاثية الأبعاد في مشهد. يوضح هذا المثال البرمجي كيفية إنشاء كائن Box، ثم تطبيق مادة PBR.
---

{{% alert color="primary" %}}

يلعب PBR دورًا رئيسيًا في مرئيات محرك الألعاب، بفضل تصويره الفعال والواقعي لتفاعلات الضوء والسطح من خلال التوهين وتشتت الضوء المنعكس. يمكن للمطورين استخدام واجهة برمجة تطبيقات Aspose.3D لتطبيق مادة PBR على الكائنات ثلاثية الأبعاد في مشهد. يوضح هذا المثال التعليمي كيفية إنشاء كائن Box، ثم تطبيق مادة PBR.

{{% /alert %}}


## **تطبيق مادة تجسيد فيزيائي قائم على الفيزياء (PBR) على صندوق**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة مشهد
var scene = new aspose.threed.Scene();

// تهيئة كائن مادة PBR
var mat = new aspose.threed.PbrMaterial();

// مادة شبيهة بالمعادن تقريبًا
mat.setMetallicFactor(0.9);

// سطح المادة خشن جدًا
mat.setRoughnessFactor(0.9);

// إنشاء صندوق سيتم تطبيق المادة عليه
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// حفظ المشهد ثلاثي الأبعاد بتنسيق USDZ
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}