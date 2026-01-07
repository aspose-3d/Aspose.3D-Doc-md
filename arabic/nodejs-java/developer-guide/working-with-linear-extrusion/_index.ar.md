---
title: العمل مع البثق الخطي
type: docs
weight: 80
url: "/ar/nodejs-java/working-with-linear-extrusion/"
description: يوفر Aspose.3D لـ Node.js عبر Java فئة LinearExtrusion، والتي تأخذ شكلًا ثنائي الأبعاد كمدخل وتمدد الشكل في البعد الثالث.
---

# **أداء البث الخطي**
Aspose.3D for Node.js عبر Java يوفر فئة `LinearExtrusion` تأخذ شكلًا ثنائي الأبعاد كمدخل وتمدد الشكل في البعد الثالث. يوضح المقتطف البرمجي التالي كيفية أداء البث الخطي:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة الشكل الأساسي المراد بثه
// تهيئة المقطع النمطي المراد بثه
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// قم بإجراء بث خطي عن طريق تمرير شكل ثنائي الأبعاد كمدخل وتمديد الشكل في البعد الثالث
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// إنشاء مشهد
var scene = new aspose.threed.Scene();

// إنشاء عقدة فرعية عن طريق تمرير البث
scene.getRootNode().createChildNode(extrusion);

// حفظ مشهد ثلاثي الأبعاد
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **الشرائح في البث الخطي**
Aspose.3D for Node.js عبر Java يوفر طريقة `setSlices` لفئة `LinearExtrusion`. تحدد طريقة setSlices عدد النقاط المتوسطة على طول مسار البث. يوضح المقتطف البرمجي التالي كيفية استخدام طريقة setSlices في البث الخطي:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة الشكل الأساسي المراد بثه
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// إنشاء مشهد
var scene = new aspose.threed.Scene();

// إنشاء عقدة يسارية
var left=scene.getRootNode().createChildNode();
// إنشاء عقدة يمينية
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// تحدد المعلمة الشرائح عدد النقاط المتوسطة على طول مسار البث
// قم بإجراء بث خطي على العقدة اليسرى باستخدام خاصية الشرائح
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// قم بإجراء بث خطي على العقدة اليمنى باستخدام خاصية الشرائح
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// حفظ مشهد ثلاثي الأبعاد
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **المركز في البث الخطي**
Aspose.3D for Node.js عبر Java يوفر طريقة `setCenter` لفئة `LinearExtrusion`. إذا تم تعيين طريقة setCenter على true، فإن نطاق البث من -Height/2 إلى Height/2، وإلا فإن البث من 0 إلى Height. يوضح المقتطف البرمجي التالي كيفية استخدام طريقة setCenter في البث الخطي:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة الشكل الأساسي المراد بثه
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// إنشاء مشهد
var scene = new aspose.threed.Scene();

// إنشاء عقدة يسارية
var left=scene.getRootNode().createChildNode();
// إنشاء عقدة يمينية
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// قم بتعيين مستوى الأرضية كمرجع
var box=new aspose.threed.Box(0.01, 3, 3);

// إذا كانت الخاصية Center صحيحة، فإن نطاق البث من -Height/2 إلى Height/2، وإلا فإن البث من 0 إلى Height
// قم بإجراء بث خطي على العقدة اليسرى باستخدام خاصيتي المركز والشرائح
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// قم بإجراء بث خطي على العقدة اليمنى باستخدام خاصيتي المركز والشرائح
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// حفظ مشهد ثلاثي الأبعاد
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **التدوير في البث الخطي**
Aspose.3D for Node.js عبر Java يوفر طريقة `setTwist` لفئة `LinearExtrusion`. تتعامل طريقة setTwist مع درجة الدوران أثناء بث الشكل. يوضح المقتطف البرمجي التالي كيفية استخدام طريقة setTwist في البث الخطي:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة الشكل الأساسي المراد بثه
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// إنشاء مشهد
var scene = new aspose.threed.Scene();

// إنشاء عقدة يسارية
var left=scene.getRootNode().createChildNode();
// إنشاء عقدة يمينية
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// تحدد الخاصية Direction اتجاه البث.
// قم بإجراء بث خطي على العقدة اليسرى باستخدام خاصيتي الدوران والشرائح
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// قم بإجراء بث خطي على العقدة اليمنى باستخدام خاصيتي الدوران والشرائح
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// حفظ مشهد ثلاثي الأبعاد
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}