---
title: Add oode التسلسل الهرمي و Share Gالبيانات الإلكترونية من Mesh بين oultiple oodes من 3D cencene
type: docs
weight: 40
url: /ar/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D ل Python via .NET يقدم لبناء التسلسل الهرمي قصيدة. Tانه Node هو لبنة أساسية من المشهد. A التسلسل الهرمي للعقد يحدد الهيكل المنطقي للمشهد ، وتوفير المحتوى المرئي عن طريق ربط هندسية ، أضواء ، والكاميرات إلى العقد.
---
## **Add oode Hفي 3D cenسين Document**
Aspose.3D ل Python via .NET يقدم لبناء التسلسل الهرمي قصيدة. Tانه Node هو لبنة أساسية من المشهد. A التسلسل الهرمي للعقد يحدد الهيكل المنطقي للمشهد ، وتوفير المحتوى المرئي عن طريق ربط هندسية ، أضواء ، والكاميرات إلى العقد.
### **Sسين rapراب Example**
A نموذج المشهد التسلسل الهرمي يشبه:

![تودو: الصورة_البديل_نص](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

In Aspose.3D ، كل `Node` مثيل يمكن أن يكون العديد من العقد الطفل ، في هذا المثال ، أنشأنا عقدة مع اثنين من العقد مكعب ، إذا قمنا بتدوير عقدة الجذر ، كما تتأثر جميع العقد الطفل:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
## **Des hare esh sh's omeeometry ata ata بين oultiple oodes**
To يقلل من ضروريات الذاكرة ، مثال واحد من [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) يمكن أن تكون ملزمة مع مختلف الحالات من [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) lass لاس. Envision التي تحتاج إلى نظام حيث يبدو أن جميع مكعبات 3D لا يمكن تمييزها ، ولكن كنت تحتاج إلى العديد من عدد كبير منهم. You يمكن أن تجنيب الذاكرة عن طريق جعل كائن واحد esh sh عندما يبدأ النظام. At هذه النقطة ، في كل مرة كنت بحاجة إلى شكل آخر ، يمكنك جعل كائن قصيدة آخر ، ثم أشر هذه العقدة إلى واحد Msh. Tله يسمى غرينيسينغ. Aspose.3D ل Python via .NET APIs تسمح للقيام غريزة.
### **مثال على ذلك**
In RTS (Rial-الوقت استراتيجية) ألعاب مثل ، يمكننا أن نرى دائما متعددة NPCs (Nعلى Pطبقة harهاركتر) مع نفس نموذج 3D ، ربما في ألوان مختلفة ، مما يجعل المحرك عادة حصة نفس شبكة البيانات الهندسة عبر مختلف NCs ، ويسمى هذه التقنية nnstancing.

{{% alert color="primary" %}}

Tهو `Mesh` يتم استخدام كائن فئة في التعليمات البرمجية. We يمكن[إنشاء كائن فئة `Mesh` كما روى هناك](/3d/ar/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Emتوضيح رمز المثال:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

In هذا المثال أنشأنا 3 العقد مكعب حصة نفس الشبكة ، كل واحد منهم لديها مواد مختلفة بألوان مختلفة.
