---
title: Split esh sh
type: docs
weight: 100
url: /ar/net/split-mesh/
description: قد يحتاج المطورون إلى تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. لن تقوم طريقة SplitMesh بتقسيم شبكة من المشهد إذا تم تعيين مادة واحدة لها. يمكن للمطورين الآن تحقيق ذلك باستخدام Aspose.3D for .NET API.
---
##  **Split ll ll hes تنسجم من cencene cener ateraterial**
قد يحتاج المطورون إلى تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. لن تقوم طريقة SplitMesh بتقسيم شبكة من المشهد إذا تم تعيين مادة واحدة لها. يمكن للمطورين الآن تحقيق ذلك باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

يحدد عدد `SplitMeshPolicy` نهج البيانات المستخدم في خوارزمية تقسيم الشبكة ، وهو يدعم سياستين ، ومشاركة البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها بياناتها الخاصة (البيانات المستخدمة فقط).

{{% /alert %}}

Tانه رمز عينة أدناه تقسيم كل تنسجم من مشهد لكل مادة. تشارك شبكة ach ach الفرعية نفس البيانات المباشرة وتختلف فقط في المؤشرات.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
##  **Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية**
Aspose.3D for .NET API يسمح للمطورين بتقسيم الشبكة عن طريق تحديد المادة يدويًا. يقوم خيار الشبكة المنقسمة بإنشاء كائنات منفصلة وستستخدم كل شبكة فرعية مادة واحدة فقط.
###  **Split Msh من ox ox**
يخلق موضوع المساعدة هذا شبكة من الصندوق للحفاظ على الرمز شامل وقصير. يمكن للمطورين إنشاء شبكة يدويًا كما روى في موضوع المساعدة هذا: [إنشاء شبكة مكعبة 3D](/3d/ar/net/create-3d-mesh-and-scene/). علاوة على ذلك ، يتكون الصندوق من 6 طائرات وستصبح كل طائرة شبكة فرعية. عينة الكود أدناه تقسم شبكة بدائية عن طريق تحديد المادة يدويًا.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
