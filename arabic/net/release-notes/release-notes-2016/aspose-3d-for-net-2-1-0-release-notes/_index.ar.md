---
title: Aspose.3D for .NET 2.1.0 tes elease oأوتس
type: docs
weight: 40
url: /ar/net/aspose-3d-for-net-2-1-0-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 2.1.0](https://www.nuget.org/packages/Aspose.3D/2.1.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-196|Separate خيارات الاستيراد وخيارات التصدير لجميع تنسيقات الملفات 3D.|New eature|
|THREEDNET-194|Eدعم xport ل Collada.|New eature|
|THREEDNET-198|Allow المستخدم للوصول إلى تقديم مستوى منخفض API.|New eature|
|THREEDNET-199|Aعقدة llow ليتم استبعادها أثناء التصدير.|Enhancement|
|THREEDNET-195|نسيج isplay غير موجود على النموذج.|Enhancement|
|THREEDNET-203|Allow Vector2/Vector3/Vector4/Quaternion لتكون قابلة للتحرير في شبكة الملكية.|Enhancement|
|THREEDNET-197|Pأوليغون قضية ثلاثية.|Bug|
|THREEDNET-202|لن يعمل iiffuse/pecpec/ misفي حالة عدم استخدام أي نسيج.|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See القائمة لأي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Adds Export من تنسيق Collada**
Uالغناء هذا الإصدار الأخير (2.1.0) ، يمكن للمطورين تصدير الملفات Collada 3D. In الإصدار السابق (2.0.0) ، لقد أضفنا بالفعل ميزة الاستيراد ، حيث يمكن للمطورين أيضا تحويل ملف Collada إلى تنسيقات الملفات الأخرى المدعومة 3D.
### **Ptions dds ooad و Save ptions ptions ل 3D File ororالحصير**
Added e قد أضاف تحميل وحفظ الخيارات لكل تنسيق ملف. يتم إعادة النظر في hey من الطبقات الفرعية الأصلية Ihey ononfig.
#### **Adds Aspose.ThreeD**
1. **ColladaSaveOptions lass**-It يحدد الإعدادات على حفظ ملف Collada 3D.
1. **Ptions iscreet3Dptions ptions oadOptions lass**-It يحدد الإعدادات على تحميل ملف حصيف 3DS.
1. **Discreet3Dptions ptions aveOptions lass**-It يحدد الإعدادات على حفظ ملف حصيف 3DS.
1. **Ptions lass lass ptions aveOptions lass**-It يحدد الإعدادات على حفظ ملف FBX.
1. **Ptions bjLoadOptions lass**-It يحدد الإعدادات على تحميل ملف bj O.
1. **ObjSaveOptions lass**-It يحدد الإعدادات على حفظ ملف bj O.
1. **Ptions lass ptions ptions oadOptions lass**-It يحدد الإعدادات على تحميل ملف STL.
1. **Ptions lass lass ptions aveOptions lass**-It يحدد الإعدادات على حفظ ملف STL.
1. **Ptions 3Dptions oadOptions lass**-It يحدد الإعدادات على تحميل ملف U3D.
1. **Ptions 3Dptions aveOptions lass**-It يحدد الإعدادات على حفظ ملف U3D.

{{% alert color="primary" %}} 

يتم وضع علامة على الطبقات الفرعية القديمة Ionononfig ، سيتم إزالتها في الإصدار الرئيسي التالي (3.0.0).

{{% /alert %}} 
### **Adds Methods إلى Aspose.ThreeD. cenسينا lass**
We لديها الزائد القلم Oوطرق ave ave في فئة cenسين. Dإيفليرز يمكن تمرير كائن تيار أو اسم الملف المباشر لاستيراد/تصدير ملف 3D باستخدام مختلف خيارات التحميل/الادخار.
### **Removal من FillDummyIndexArray roroperty من Aspose.ThreeD. orormat. FBonononfig lass**
Tلم يتم استخدام ممتلكاته.
### **Detect ype من 3D ile ile**
The Detect طريقة Aspose.ThreeD.FileFormat فئة يمكن التعرف على نوع أي ملف معتمد 3D.
#### **Ptions dds Detect ، ptions reateLoadOptions و rereateSaveOptions في Aspose.ThreeD. 07ileFormat lass**
After التعرف على نوع ملف 3D ، يمكن للمطورين إنشاء وصفات oadOptions والأشياء aveOaveOباستخدام reateLoadOالوصفات وreateSaveOطرق الوصفات من فئة orileFormat.
### **Adds Expackded roroperty إلى Aspose.ThreeD.Entity و Aspose.ThreeD.**
يسمح It بإزالة كيان أثناء التصدير.
### **Adds Aspose.ThreeD**
Tانه يجعل الدول توفر المعلمات ل GPU لتمزيق مثلثات إلى بكسل.

{{% alert color="primary" %}} 

Encapsulation من الأجهزة تجعل الدول ، يمكن العثور على معلومات تفصيلية في وثائق[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Assx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). اسبكس) و[Vأولكان](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Adds ader hader APIs**
The Shader AIIs تحديد كيفية تحويل المثلثات من الفضاء العالمي إلى مساحة الشاشة وحساب لون بكسل النهائي في الجانب GPU.
#### **Adds فئة مجردة Aspose.ThreeD. ender ender. hadhaderSource والفئة الفرعية Aspose.ThreeD.**
The GLSource ource يقول ren، رمز المصدر هو لغة التظليل OpenGL ، ويمكن تجميعها إلى Aspose.ThreeD.
#### **Adds Aspose.ThreeD.**
Tانه Sهادر الاستثناءات ذات الصلة ، وتستخدم أساسا في لغة شادر تجميع وربط المرحلة.
#### **Adds Aspose.ThreeD. ender ender. hadhadrogram lass**
It هو برنامج shader مجمعة.
#### **Add Aspose.ThreeD. ender ender. hadhaderVariable lass**
It يحدد المتغيرات المستخدمة في شادر.
#### **Adds و Eنوم lass لاس Aspose.ThreeD.**
يستخدم It لتحديد الدلالي متغير شادر ، Aspose.3D المستأجر إعداد القيم المتغيرة شادر تلقائيا يعتمد على الدلالات.
### **Aدس ffer ffer ffer PIs**
Tهو المخازن المؤقتة توفير تعريف والبيانات من المثلثات.
#### **Adds و 07nterface Aspose.ThreeD.**
It هو واجهة قاعدة ل InndexBuyee و ererertexBuvec.
#### **Adds nnterfaces Aspose.ThreeD.**
Hey يا مخازن الأجهزة الحالية لتخزين مؤشرات الهندسة.
#### **Adds و Eنوم Aspose.ThreeD. ender اندر. nndexDataType**
Tانه datatype من مؤشرات الهندسة.
### **Adds ender ender ender Is**
#### **Adds و 07nterface Aspose.ThreeD.**
An الكائن الذي يدعم تقديم يجب تنفيذ هذه الواجهة.
#### **Added an nnum Aspose.ThreeD.**
Tانه نوع بدائي لرسم.
#### **Adds و Enum Aspose.ThreeD.**
Aspose.3D API يستخدم طابور تقديم لإدارة سير العمل ، ويستخدم هذا لتقديم عملية تقديم إلى قائمة انتظار تقديم محددة.
#### **Adds Aspose.ThreeD.**
فئة ase briلربط طراز Aspose.3D API بموارد الأجهزة ، يتم استخدام هذا من قبل Aspose.3D داخليًا ، ولكنه يتعرض لإطلاق العنان للقوة الكاملة لعرض Aspose.3D.
#### **Adds Aspose.ThreeD.**
A Sub فئة من RenderResource ، ولكن التركيز على تقديم.
#### **Adds Aspose.ThreeD. nntities. ManualEntity lass**
Tيجب على المستخدم استخدام هذه الفئة لتنفيذ كيانها الخاص الذي يدعم تقديم ، هذه الفئة تغليف تفاصيل تقديم العمليات وإدارة الموارد.
### **Thodds Multiple riريانغتوال ثود في Aspose.ThreeD. nntities.**
Mخام الزائد لتبسيط استخدام الوظيفة الأصلية.
### **Adds rereateVertexBuyee ، CreateIndexBuvec، CreateTextureUnit ، CreateRenderState و rereateShaerProgram Methods في Aspose.ThreeD.**
### **Adds indindRenderState ، DrouIndexed ، Dالخام و uubmitRenderTاسأل thoethods في Aspose.ThreeD.**
### **Adds enenderSage و Shader roroperties في Aspose.ThreeD.**
