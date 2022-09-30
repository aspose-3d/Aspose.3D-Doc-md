---
title: Add oode التسلسل الهرمي و Share Gالبيانات الإلكترونية من Mesh بين oultiple oodes من 3D cencene
type: docs
weight: 20
url: /ar/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java لديه دعم لبناء التسلسل الهرمي من القلادات. The oode هو لبنة البناء الأساسية من المشهد 3D والتسلسل الهرمي للعقد يحدد الهيكل المنطقي للمشهد 3D ، وتوفير محتوى مرئي عن طريق ربط الهندسة والأضواء والكاميرات إلى العقد.
---
## **Add oode Hفي 3D cenسين Document**
Aspose.3D for Java لديه دعم لبناء التسلسل الهرمي من القلادات. The `Node` هو لبنة البناء الأساسية من المشهد 3D والتسلسل الهرمي للعقد يحدد الهيكل المنطقي للمشهد 3D ، وتوفير محتوى مرئي عن طريق ربط الهندسة والأضواء والكاميرات إلى العقد.
### **Sسين rapراب Example**

In Aspose.3D ، كل `Node` مثيل يمكن أن يكون العديد من العقد الطفل ، في هذا المثال ، أنشأنا عقدة مع اثنين من العقد مكعب ، إذا قمنا بتدوير عقدة الجذر ، كما تتأثر جميع العقد الطفل:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **Des hare esh sh's omeeometry ata ata بين oultiple oodes**
In الطلب على تقليل ضروريات الذاكرة ، يمكن أن تكون ملزمة مثيل واحد من `Mesh` lass لاس إلى حالات مختلفة من `Node` lass لاس. Envision التي تحتاج إلى نظام حيث يبدو أن جميع مكعبات 3D لا يمكن تمييزها ، ولكن كنت تحتاج إلى العديد من عدد كبير منهم. You يمكن أن تجنيب الذاكرة عن طريق جعل كائن واحد esh sh عندما يبدأ النظام. At هذه النقطة ، في كل مرة كنت بحاجة إلى شكل آخر ، يمكنك جعل كائن ode آخر ، ثم أشر هذه العقدة إلى واحد `Mesh`. Tله يسمى غرينيسينغ. Aspose.3D for Java allow PIs تسمح للقيام بتثبيت.
### **مثال على ذلك**
In RTS (Rial-الوقت استراتيجية) ألعاب مثل ، يمكننا أن نرى دائما متعددة NPCs (Nعلى Pطبقة harهاركتر) مع نفس نموذج 3D ، ربما في ألوان مختلفة ، مما يجعل المحرك عادة حصة نفس شبكة البيانات الهندسة عبر مختلف NCs ، ويسمى هذه التقنية nnstancing.

{{% alert color="primary" %}} 

Tهو `Mesh` يتم استخدام كائن فئة في التعليمات البرمجية. We يمكن[إنشاء كائن فئة Mesh كما روى هناك](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Emتوضيح رمز المثال:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


In هذا المثال أنشأنا 3 العقد مكعب حصة نفس الشبكة ، كل واحد منهم لديها مواد مختلفة بألوان مختلفة.
