---
title: تحديد خيارات تحميل ملف ثلاثي الأبعاد
type: docs
weight: 10
url: "/ar/nodejs-java/specify-3d-file-load-options/"
description: هناك عدة تحميلات لأسلوب Scene.open أو تحميلات منشئ فئة Scene التي تقبل نسخة LoadOptions.
---

## **خيارات تحميل ملفات ثلاثية الأبعاد**
هناك عدة عمليات تحميل زائدة للطريقة Scene.open أو عمليات تحميل زائدة لفئة Scene تتقبل نسخة من LoadOptions. يجب أن تكون نسخة من فئة مشتقة من فئة LoadOptions. لكل تنسيق تحميل فئة مقابلة تحتفظ بخيارات التحميل لهذا التنسيق، على سبيل المثال هناك ColladaSaveOptions لتنسيق الحفظ FileFormat.COLLADA.
### **استخدام خيارات Discreet 3DS Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Discreet 3DS.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// تعيين ما إذا كان سيتم استخدام التحويل المحدد في الإطار الأول من مسار الرسوم المتحركة.
loadOpts.setApplyAnimationTransform(true);

// عكس نظام الإحداثيات
loadOpts.setFlipCoordinateSystem(true);

// إعطاء الأولوية لاستخدام اللون المصحح الغاما إذا كان ملف 3ds يوفر كلاً من اللون الأصلي واللون المصحح الغاما.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **استخدام خيارات Obj Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Obj ثلاثي الأبعاد.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// استيراد المواد من ملف مكتبة المواد الخارجية
loadObjOpts.setEnableMaterials(true);

// عكس نظام الإحداثيات.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **استخدام خيارات STL Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة كائن
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// عكس نظام الإحداثيات.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **استخدام خيارات U3D Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة كائن
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// عكس نظام الإحداثيات.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **استخدام خيارات glTF Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تعيين خيارات التحميل
var loadOpt = new aspose.threed.GltfLoadOptions();

// القيمة الافتراضية هي true، عادة لا نحتاج إلى تغييرها. سيقوم Aspose.3D تلقائيًا بعكس إحداثي V/T النسيج أثناء التحميل والحفظ.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **استخدام خيارات Ply Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة كائن الفئة Scene
var scene = new aspose.threed.Scene();

// تهيئة كائن
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// عكس نظام الإحداثيات.
loadPLYOpts.setFlipCoordinateSystem(true);

// تحميل نموذج Ply ثلاثي الأبعاد
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **استخدام خيارات DirectX X Load**
يعرض الكود أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف DirectX X.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة كائن الفئة Scene
var scene = new aspose.threed.Scene();

// تهيئة كائن
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// عكس نظام الإحداثيات.
loadXOpts.setFlipCoordinateSystem(true);

// تحميل ملف X ثلاثي الأبعاد
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **استخدام خيارات FBX Load**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

//سيؤدي هذا إلى إخراج جميع الخصائص المحددة في GlobalSettings في ملف FBX.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}