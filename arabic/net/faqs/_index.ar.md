---
title: FAQs
type: docs
weight: 190
url: /ar/net/faqs/
description: الأسئلة المتداولة حول Aspose.3D لـ. شبكة.
---
####  **Q: كيف يمكنك تحريك FBX أو خاصية خاصة بتنسيق 3D أخرى لم يتم تعريفها في Aspose.3D ؟**
* A *: قم بإنشاء خاصية ديناميكية على الكائن الهدف ، وقم بتنفيذ خاصية الرسوم المتحركة على الخاصية الديناميكية ، نظرًا لأن الخاصية تعتمد على تنسيق ملف ملموس ، Aspose. لا يمكن أن يضمن 3D أن الرسوم المتحركة يمكن أن تعمل عند حفظ المشهد إلى نوع تنسيق مختلف.
####  **Q: لماذا لا تعمل الرسوم المتحركة على عقدة جذر المشهد عند التسلسل إلى ملف FBX ؟**
* A ، *: لا يسمح لك تنسيق FBX بالوصول إلى خصائص عقدة الجذر ، وبالتالي لن تعمل الرسوم المتحركة.
####  **س: لماذا قمت بتغيير معلومات الأصول على المشهد ، ومحاولة استيراد ملف FBX الذي تم إنشاؤه إلى 3ds max ، فقد تم فقدان هذه المعلومات بالكامل ؟**
*A**: 3Ds MAX or some other softwares can only import FBX file, but not open the FBX file, that means it allows you to import multiple FBX inside one scene, if the asset info can be applied to the current scene, then your original scene info may be overwritten by importing, so that’s 3Ds MAX’s design policy to not import the scene’s asset info.


####  **Q: تتكون العقدة من شبكات متعددة (للزجاج ، الإطار ، إلخ). كل هذه الشبكات توجد في قائمة الكيانات للعقدة. كيفية إضافة مادة إلى كل هذه العقد (المادة هي اللون فقط) ؟**
* A ، *: الحل الأفضل يجب أن يخلق عقد فرعية لكل شبكة ، وتعيين مادة مختلفة لكل عقدة فرعية.