---
title: Create 3D Msh و cencene
type: docs
weight: 40
url: /ar/java/create-3d-mesh-and-scene/
description: يتم تعريف A esh sh من خلال مجموعة من نقاط التحكم والعديد من المضلعات على الوجهين n حسب الحاجة. Tمقالته يوضح كيفية تعريف esh sh.
---
## **Ate reate a 3D Cube esh esh**
يتم تعريف 07`Mesh` من خلال مجموعة من نقاط التحكم والعديد من المضلعات على الوجهين n حسب الحاجة. Tمقالته يوضح كيفية تعريف `Mesh`.

In الطلب لإنشاء سطح `Mesh` ، ونحن بحاجة إلى تحديد نقاط التحكم والمضلعات على النحو التالي:

- [Define Cأونتول oin](/3d/ar/java/create-3d-mesh-and-scene-html/)
- [Olyreate olyأوليغونز مع PolygonBuilder lass لاس](/3d/ar/java/create-3d-mesh-and-scene-html/)
- [Olyreate olyأوليغونز](/3d/ar/java/create-3d-mesh-and-scene-html/)

Here مثال على إرفاق مادة هونغ Pإلى عقدة مكعب:
### **Define Cأونتول oin**
يتكون شبكة A من قبل مجموعة من نقاط التحكم في الفضاء ، والمضلعات لوصف سطح الشبكة ، لإنشاء شبكة ، ونحن بحاجة إلى تحديد نقاط التحكم:

{{% alert color="primary" %}} 

Tانه السيطرة على نقاط من جميع هندسية في Aspose.3D استخدام تنسيق متجانس ، لذلك انها `Vector4` بدلا من `Vector3` في رمز المثال.

{{% /alert %}} 

**Example:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



### **Olyreate olyأوليغونز**
Tانه نقاط التحكم ليست قابلة للتأجير ، لجعل مكعب مرئية ، ونحن بحاجة إلى تحديد المضلعات في كل جانب:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



### **Olyreate olyأوليغونز مع PolygonBuilder lass لاس**
We يمكن أيضا تحديد المضلع بواسطة vertices مع PolygonBuilder الفئة:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Now انها الانتهاء ، لجعل شبكة مرئية ، ونحن بحاجة إلى إعداد عقدة لذلك.
## **How إلى ririesh**
شبكة ريانغتوليت غير مفيدة لصناعة اللعبة لأن الثلاثي هو البدائية الوحيدة المدعومة التي تدعم الأجهزة GPU (يتم تقسيم البيانات غير الثلاثية في مستوى السائق ، وهو غير فعال في تقديم في الوقت الحقيقي)

{{% alert color="primary" %}} 

In هذا الإصدار نحن مثلثات فقط المضلعات لأنه مطلوب من قبل 3ds تصدير الملفات ، يتم فقدان طبيعية/uvs وغيرها من عناصر فيرتكس خلال هذا الإجراء ، يمكننا تنفيذ هذا في المستقبل.

{{% /alert %}} 

في هذا المثال ، نقوم بتثليث ملف esh esh عن طريق استيراد ملف FBX وحفظه بتنسيق FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
## **Ate reate a 3D Cube cencene**
Tموضوعه يوضح كيفية إضافة هندسة esh esh إلى مشهد 3D. Tانه مثال رمز يضع مكعب وحفظ المشهد 3D في تنسيقات الملفات المدعومة.
### **Rereate Cube oode**
عقدة A غير مرئية ، ولكن يمكن تقديم الهندسة المرفقة بالعقدة.

{{% alert color="primary" %}} 

يتم استخدام كائن الطبقة في الرمز. We يمكن[إنشاء كائن فئة Mesh كما روى هناك](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Example:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

NOTE: عادة ما يتم تجاهل الكيانات المرتبطة بعقدة الجذر في CAD/07softwM برامج ، لذلك نحن بحاجة إلى إنشاء عقدة جديدة لتقديم الهندسة.

{{% /alert %}}
