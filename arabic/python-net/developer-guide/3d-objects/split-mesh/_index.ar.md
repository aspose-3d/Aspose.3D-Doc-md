---
title: Split esh sh
type: docs
weight: 100
url: /ar/python-net/split-mesh/
description: قد تتطلب opers إيفلين تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. Tانه Sطريقة plitMsh لن تقسيم شبكة من المشهد If تم تعيين مادة واحدة. يمكن الآن تحقيق ذلك باستخدام Aspose.3D ل Python via .NET API.
---
## **Split ll ll hes تنسجم من cencene cener ateraterial**
قد تتطلب opers إيفلين تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. The `split_mesh` طريقة لن تقسيم شبكة من المشهد If تم تعيين مادة واحدة. Dإيفلين يمكن الآن تحقيق ذلك باستخدام[Aspose.3D ل Python via .NET](https://products.aspose.com/3d/python-net/)API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum يحدد سياسة البيانات المستخدمة في خوارزمية تقسيم الشبكة ، فإنه يدعم اثنين من السياسات ، وتبادل البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها البيانات الخاصة بها (البيانات المستخدمة فقط).

{{% /alert %}}

Tانه رمز عينة أدناه تقسيم كل تنسجم من مشهد لكل مادة. تشارك شبكة ach ach الفرعية نفس البيانات المباشرة وتختلف فقط في المؤشرات.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
## **Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية**
Aspose.3D Python via .NET API يسمح للمطورين بتقسيم شبكة عن طريق تحديد المواد يدويًا. Tانه تقسيم شبكة الخيار يخلق كائنات منفصلة وكل شبكة فرعية سوف تستخدم مادة واحدة فقط.
### **Split Msh من ox ox**
Tموضوع مساعدته يخلق شبكة من صندوق للحفاظ على رمز شامل وقصير. Dإيفليرز قد بناء شبكة يدويا كما روى في هذا الموضوع مساعدة:[Ate reate a 3D Cube esh esh](/3d/ar/python-net/create-3d-mesh-and-scene/). Furthermore ، ويتكون صندوق من 6 طائرات وسوف تصبح كل طائرة شبكة فرعية. Tانه رمز عينة أدناه تقسيم شبكة بدائية عن طريق تحديد يدويا المواد.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
