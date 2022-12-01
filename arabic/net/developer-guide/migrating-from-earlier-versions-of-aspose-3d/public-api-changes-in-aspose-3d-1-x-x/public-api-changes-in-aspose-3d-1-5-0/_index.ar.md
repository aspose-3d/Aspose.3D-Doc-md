---
title: Public API hangمعلقة في Aspose.3D 1.5.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Contents Sأوماري**

- [Convert ririmitive إلى esh esh و rereate cencene من Primitive 3D oodels](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Split esh sh](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Emoemoval من تنسيق Distreet3D.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Adds Discreet3DS التنسيق.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Property dds خاصية liplipCotrademateSyالجذعية في الفئة Aspose.ThreeD. orormat. Universal3Dononfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 1.4.0 إلى 1.5.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Convert ririmitive إلى esh esh و rereate cencene من Primitive 3D oodels**
**يتم إضافة ليزر arious arious ، روح Mو roperties P**

- **واجهة Adds Aspose.ThreeD. nntities.** 
-يمكن تحويل فئة ny ny التي تنفذ هذه الواجهة إلى mesh أثناء التصدير إلى أي تنسيقات ملفات 3D.
- **Adds الفئة Aspose.ThreeD. nntities.** 
-It مشتق من فئة Entity وأيضا الطبقة الأساسية لجميع الطبقات البدائية.
- **Adds الفئة Aspose.ThreeD. nntities. ox ox/Cيندر/Pلين/Sفير/Torus.** 
-These يمكن استخدامها لتحديد المشهد مع البدائية بسيطة. Dإيفلين يمكن أيضا تحويلها إلى شبكة تلقائيا.

وتشمل ريميفيرس Pالعديد من الأشياء الأساسية والأكثر استخداما مثل صندوق ، المجال ، الطائرة ، اسطوانة ، و توروس. قد Dإيفلين أيضا تحويلها إلى شبكة لأغراض التعديل. These تساعد المواضيع توضيح كيفية القيام بذلك:[Convert ririmitive إلى Msh](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)و[Convert ririmitive إلى Msh](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex**
**يتم إضافة ليزر arious arious ، روح Mو roperties P**

- **Adds فئة Aspose.ThreeD. nntities. TriMesh/TriMesh<T>** 
-Tريبليش/Tريبليش<T>يحتوي على تعريف الشبكات القائمة على المثلث مع تخطيط الذاكرة المخصصة ، وهو أمر مفيد عندما يتطلب المطور لتحويل المشهد إلى تنسيقات الملفات الخاصة بهم أو في تقديم.
- **هيكل Adds Aspose.ThreeD. tiliتيليتيز. Fecector2/FVector3/Fecector4** 
-الطبقات These الحالية مكونات ناقلات في تعويم. Only عدد قليل من vector الحديثة vector U يدعم ناقلات مزدوجة الدقة ، وأنواع تعويم واحدة الدقة هي أكثر الترحيب في الوقت الحقيقي تقديم العالم. سوف تتعايش بدائل ese hese مع الأصلي Vector2/Vector3/Vector4 لأنها تلعب أدوار مختلفة في Aspose.3D. يستخدم ououble-الدقة أساسا لتخزين بيانات النموذج لأنه يحتوي على خطأ أقل تراكمًا. يتم استخدام Single-الدقة بشكل رئيسي في تقديم أو تحويل تنسيقات الملفات الخاصة بالمستخدم لأنه يحتوي على قبول وأداء أفضل. قدم We هذه المجموعة من ناقلات في Aspose.3D 1.5 لأننا أضفنا الدعم لتخطيط فيرتكس مخصص ، حيث سيتم استخدام ناقلات تعويم بشكل متكرر.
- **Attribudds سمة الفئة Aspose.ThreeD. tiliتيليتيز.** 
-Dإيفلوبر يمكن تحديد هيكل مخصص ل فيرتكس ، واستخدام هذه السمة للاحتفال الدلالية من الحقول.
- **Adds الفئة Aspose.ThreeD. tiliتيليتيز.** 
-Describes t يصف تخطيط الذاكرة من قمة الرأس.
- **Adds enum Aspose.ThreeD.** 
-أنواع These enum توضح نوع بيانات حقل فيرتكس والدلالية على التوالي.
- **Adds الفئة Aspose.ThreeD. tiliتيليتيز.** 
-Describes t يصف كل حقل في تخطيط الذاكرة المخصصة من erertex.
- **Adds الفئة Aspose.ThreeD. tiliتيليتيز. erertex** 
-يمكن استخدام It للوصول إلى القشرة الخام في TriMesh/TriMesh<T>

Dإيفليرز قد تحويل أي كائن شبكة إلى شبكة مثلث مع تخطيط الذاكرة مخصص من فيرتكس. Tانه حزم البرمجيات البيانية وأجهزة الأجهزة تعمل بشكل أكثر كفاءة على مثلثات. Tموضوع مساعدته يوضح كيفية القيام بذلك:[Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Split esh sh**
**يتم إضافة ليزر arious arious ، روح Mو roperties P**

- **Adds enum Aspose.ThreeD. nntities. plplitMeshPolicy** 
-It يحدد سياسة البيانات المستخدمة في خوارزمية تقسيم شبكة ، ونحن نؤيد اثنين من السياسات ، وتبادل البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها البيانات الخاصة بها (Oالبيانات المستخدمة nly).
- **Adds 3 طرق plplitMesh إلى Aspose.ThreeD. nntities.** 
1. hes تنسجم plit على عقدة محددة إلى شبكات فرعية حسب تعريف المواد.
1. Split كل شبكة في المشهد معين إلى الشبكات الفرعية حسب تعريف المواد.
1. pplit شبكة معينة إلى الشبكات الفرعية حسب تعريف المواد.
- **Property dds خاصية liplipCotrademateSyالجذعية في الفئة Aspose.ThreeD. orormat. Universal3Dononfig** 
-It يسمح للمستخدمين الوجه نظام تنسيق U3D أثناء الاستيراد أو التصدير.

قد تتطلب evelevelتقسيم شبكة تلقائيا عن طريق المواد ، بحيث يتم استخدام كل شبكة فقط مادة واحدة أو شبكة الانقسام عن طريق تحديد المواد. These تساعد المواضيع توضيح كيفية القيام بذلك:[Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)و[Split ll ll hes تنسجم من cencene cener ateraterial](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Emoemoval من تنسيق Distreet3D.**
يتم وضع علامة تنسيق Distreet3Dكما عفا عليها الزمن بسبب موجة غير صحيحة.
### **Adds Discreet3DS التنسيق.**
Discreet3DS تم تقديم شكل.
### **Property dds خاصية liplipCotrademateSyالجذعية في الفئة Aspose.ThreeD. orormat. Universal3Dononfig**
It يسمح للمستخدمين flip نظام التنسيق من U3D أثناء الاستيراد أو التصدير.
