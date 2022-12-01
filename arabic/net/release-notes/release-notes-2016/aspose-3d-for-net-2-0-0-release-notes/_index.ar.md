---
title: Aspose.3D for .NET 2.0.0 tes elease tes أوتس
type: docs
weight: 50
url: /ar/net/aspose-3d-for-net-2-0-0-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 2.0.0](https://www.nuget.org/packages/Aspose.3D/2.0.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-113|Import دعم Collada|ميزة ew ew|
|THREEDNET-183|Post-آثار المعالجة|ميزة ew ew|
|THREEDNET-191|Use Vector4 لتمثيل إحداثيات UU.|Enhancement|
|THREEDNET-189|Render قد تحطم التطبيق على منصة 64bit|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See القائمة لأي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Rial-تقديم الوقت**
It يسمح للمطورين لأداء تقديم عالية الأداء في الوقت الحقيقي على إطار GUI مثل orinForms ، انها GUindependent إطار مستقل ، وبالتالي فإن الأطر GGGالأخرى يجب أيضا دعم هذا.
#### **Adds Collada تنسيق**
In هذا الإصدار (2.0.0) ، يمكن للمطورين استيراد الملفات Collada 3D ، لذلك يتم إضافة Collada خاصية في Aspose.ThreeD.
#### **Classes dds Aspose.ThreeD**
The oundh9 ingBox و oundh9 ingBoxExالخيمة الطبقات تمثل صندوق الحدود من عقدة 3D. قد إعادة تعيين الكاميرا ، وحساب الارتفاع من صندوق الحدود. Tانه لانهائي أو لاغية صندوق الحدود يعني المشهد ليس لديه هندسية وضبط فقط ارتفاع الكاميرا عندما يكون محدود.
#### **Rاسم نوع Aspose.ThreeD.UpVector إلى Aspose.ThreeD.Axis**
تم إعادة تسمية فئة pVector إلى فئة Axis.
#### **Adds Aspose.ThreeD.**
Tأنه يتم لف استثناءات من المستأجر الداخلي كما xcriverException.
#### **Adds Aspose.ThreeD.**
Tيتم طرح استثنائه في حين فشل في تهيئة مقدم العرض ، على سبيل المثال لتهيئته على جهاز كمبيوتر لا يدعم الأجهزة OpenGL 4.0.
#### **Adds Aspose.ThreeD. ender اندر. Renderer الفئة**
Rereate كائن محدد الرأس وجعل نافذة من مقبض النافذة الأصلي. Ight ight الآن نحن ندعم فقط مقبض النافذة الأصلي من Microsoft Windows. We سوف تدعم المزيد من المنصات في المستقبل. The rereateRenderer طريقة من فئة enenderer يخلق جهاز OpenGL-backend renderer وسيتم إجراء بعض التبادلات الداخلية. Wالدجاجة المستأجر يخرج من نطاق ، سيتم أيضا التخلص من موارد الأجهزة غير المدارة.
#### **Adds Aspose.ThreeD. ender اندر. Viewport الفئة**
Aspose.3D API يدعم ثلاثة أنواع من المناظر. Since الهدف جعل أي وجهة نظر من هذه الأنواع.
#### **Classes dds Aspose.ThreeD.**
- IenenderTarget هي واجهة قاعدة من IenenderTexture/IenenderWindow.
- IenenderTexture يسمح لتقديم المشهد إلى واحد أو أكثر من القوام (القوام تقع في ذاكرة الفيديو ويمكن نقلها إلى ذاكرة النظام).
- IenenderWindow يسمح لتقديم المشهد إلى نافذة في الوقت الحقيقي.
#### **Classes dds Aspose.ThreeD. Rاندر. IexextureUnit و Aspose.ThreeD.**
IexextureUnit هو في الواقع عينة الملمس في الجانب GPside و بيانات الملمس في CPU أو GPU الذاكرة.
#### **Adds Aspose.ThreeD.**
تسمح فئة roostProcessing للمطورين بتطبيق فلتر معالجة الصور في الوقت الحقيقي على الصورة المقدمة. In هذا الإصدار ، لقد قدمنا 4 المدمج في آثار ما بعد المعالجة. سوف تسمح We للمطورين بالحصول على خوارزمية ما بعد المعالجة المخصصة الخاصة بهم في الإصدار المستقبلي.
#### **Adds Aspose.ThreeD.**
It يساعد في تقديم مشهد إلى القوام أو النافذة في الوقت الحقيقي.
#### **Adds Aspose.ThreeD.**
It يحدد المعلمات حول كيفية إنشاء الهدف تقديم مثل بت اللون ، بت عمق ، بت الاستنسل ، التخزين المؤقت المزدوج.
#### **يتم إضافة طرق ddddData إلى Aspose.ThreeD.**
لقد تغيرت فئة قاعدة he he erertexEleرقيق V من اللوحة الرئيسية<Vector2>إلى VertexE<Vector4>، فإنه سيتم تخزين فقط Vector4 منذ 2.0.0 ، لذلك تم إضافة طريقتين مساعد للسماح للمستخدم لإضافة قائمة من Vector2 و Vector3 إلى erertexEleentUV ، فإنه سيتم داخليا توسيع Vector2/Vector3 إلى Vector4 وترك بقية المجالات صفر:
#### **Changes roperty التغييرات في الفئة Aspose.ThreeD.FileFormat**
يتم تغيير خصائص ormat من عدد صحيح إلى عدد صحيح.
#### **يتم إضافة طريقة ox etBh9 ingBox إلى Aspose.ThreeD.**
It يسمح للمطورين للحصول على صندوق الحدود الانحياز محور.
