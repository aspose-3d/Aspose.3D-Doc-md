---
title: Split esh sh
type: docs
weight: 10
url: /ar/java/split-mesh/
description: Aspose.3D for Java API لديه دعم لتقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. Tانه Sطريقة plitMsh لن تقسيم شبكة من المشهد ، إذا كان قد تم تعيين مادة واحدة. يمكن تحقيق It باستخدام Aspose.3D for Java API.
---
## **Split جميع شبكات من Sسين cener aterالمواد**
Aspose.3D for Java API لديه دعم لتقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. Tانه Sطريقة plitMsh لن تقسيم شبكة من المشهد ، إذا كان قد تم تعيين مادة واحدة. يمكن تحقيق It باستخدام Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum يحدد سياسة البيانات المستخدمة في خوارزمية تقسيم الشبكة ، فإنه يدعم اثنين من السياسات ، وتبادل البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها البيانات الخاصة بها (البيانات المستخدمة فقط).

{{% /alert %}} 

Tانه رمز عينة أدناه تقسيم كل تنسجم من مشهد لكل مادة. تشارك شبكة ach ach الفرعية نفس البيانات المباشرة وتختلف فقط في المؤشرات.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
## **Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية**
Aspose.3D for Java API لديه دعم لتقسيم شبكة عن طريق تحديد المواد يدويا. Tانه تقسيم شبكة الخيار يخلق كائنات منفصلة وكل شبكة فرعية سوف تستخدم مادة واحدة فقط.
### **Split esh sh من ox ox**
Tموضوع مساعدته يخلق شبكة من صندوق للحفاظ على رمز شامل وقصير. Dإيفليرز قد بناء شبكة يدويا كما روى في هذا الموضوع مساعدة:[Ate reate a 3D Cube esh esh](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Furthermore ، ويتكون صندوق من 6 طائرات وسوف تصبح كل طائرة شبكة فرعية. Tانه رمز عينة أدناه تقسيم شبكة بدائية عن طريق تحديد المواد يدويا.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
