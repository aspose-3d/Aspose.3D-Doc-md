---
title: القيود وفروق API
type: docs
weight: 60
url: /ar/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: حدود Aspose.3D for Node.js via Java واختلافات api
---
##  **الاختلافات العامة API**
تعرض القائمة التالية (مع مقاطع رمز العينة) بعض الاختلافات بين Aspose.3D for Java و Aspose.3D for Node.js via Java APIs.
###  **مكتبة مستوردة (مقارنات الحزم)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
###  **مستهل مشهد جديد**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **تهيئة الكائن**

**Aspose.3D for Java**

{{< highlight "java" >}}

Plane plane = new Plane();

plane.setUp(new Vector3(1, 1, 3));

{{< /highlight >}}

**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var plane=new aspose.threed.Plane();

plane.setUp(new aspose.threed.Vector3(1, 1, 3));

{{< /highlight >}}

##  **قيود أخرى بقيمة Aspose.3D for Node.js via Java API مقارنة بـ Aspose.3D for Java API**
1. استيراد/تصدير البيانات من صفيف ، ArrayList ، ResultSet وما إلى ذلك غير مدعوم.
1. الطباعة غير مدعومة.

