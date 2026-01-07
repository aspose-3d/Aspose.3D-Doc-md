---
title: إضافة معلومات الأصول إلى المستند ثلاثي الأبعاد
type: docs
weight: 10
url: "/ar/nodejs-java/add-asset-information-to-3d-document/"
description: البيانات الوصفية هي معلومات منظمة تصف أو تشرح أو تحدد موقع أو تسهل استرجاع أو إدارة مورد معلوماتي. يوفر Aspose.3D لـ Node.js عبر Java API دعمًا لتعريف البيانات الوصفية للمشهد.
---

## **إضافة معلومات الأصول إلى مستند ثلاثي الأبعاد**
البيانات الوصفية هي معلومات منظمة تصف أو تشرح أو تحدد موقع أو تسهل استرجاع أو استخدام أو إدارة مورد معلوماتي. Aspose.3D لـ Node.js عبر Java API يدعم تعريف البيانات الوصفية للمشهد.
### **تعريف البيانات الوصفية للمشهد**
تنتج عروض ثلاثية الأبعاد كميات هائلة من البيانات الوصفية ومعلومات الصور. البيانات الوصفية هي أصل وجزء من العرض.

1. تهيئة مشهد ثلاثي الأبعاد باستخدام فئة `Scene`.
1. تعيين اسم التطبيق/الأداة.
1. تعيين اسم المورد/البائع.
1. تعيين وحدة القياس.
1. تعيين عامل مقياس وحدة القياس.
1. حفظ المشهد ثلاثي الأبعاد بتنسيق الملف المدعوم.

في هذا المثال، نفترض أن المشهد تم إنشاؤه بواسطة أداة CAD تسمى "Egypt" وقد صممها "Manualdesk":

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize a 3D scene
var scene = new aspose.threed.Scene();

// Initialize the Box object
var box=new aspose.threed.Box();

// Add the Box object to the scene
scene.getRootNode().createChildNode(box);

// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");

// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");

// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}