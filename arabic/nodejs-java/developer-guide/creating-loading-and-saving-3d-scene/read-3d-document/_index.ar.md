---
title: قراءة مستند ثلاثي الأبعاد
type: docs
weight: 30
url: "/ar/nodejs-java/read-3d-document/"
description: يدعم Aspose.3D لـ Node.js عبر Java API قراءة أنواع مختلفة من مستندات ثلاثية الأبعاد.
---

## **قائمة بتنسيقات 3D المدعومة (استيراد)**
Aspose.3D for Node.js عبر Java API يدعم قراءة أنواع مختلفة من مستندات 3D. تساعد المُنشئات المتاحة في فئة `Scene` على فعل ذلك وتقبل سلسلة مسار ملف صالح. التنسيقات القابلة للقراءة المدعومة هي:

1. FBX 7.5 (ASCII, Binary)
1. FBX 7.4 (ASCII, Binary)
1. FBX 7.3 (ASCII, Binary)
1. FBX 7.2 (ASCII, Binary)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCII, Binary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

تكتشف المُنشئات في فئة Scene تنسيق مستند 3D داخليًا.
## **استيراد مستند 3D**
Aspose.3D for Java API يدعم استيراد أنواع مختلفة من مستندات 3D لأغراض التعديل والإضافة والمعالجة.
### **قراءة مشهد 3D: نماذج برمجية**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// تهيئة كائن فئة Scene
var scene = new aspose.threed.Scene();

// تحميل مستند 3D موجود
scene.open( "document.obj");

{{< /highlight >}}