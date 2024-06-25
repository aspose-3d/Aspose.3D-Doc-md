---
title: العام API التغييرات في Aspose.3D 1.5.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Contents Sأوماري**

- [تحويل بدائي إلى شبكة وإنشاء مشهد من النماذج البدائية 3D](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Split esh sh](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Emoemoval من تنسيق Distreet3D.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [يضيف تنسيق Discreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [يضيف خاصية flipodrunatesystem في الفئة Aspose.ThreeD. Fults. Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

توضح هذه الوثيقة التغييرات إلى Aspose.3D API من الإصدار 1.4.0 إلى 1.5.0 ، والتي قد تهم مطوري الوحدات/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **تحويل بدائي إلى شبكة وإنشاء مشهد من النماذج البدائية 3D**
**يتم إضافة ليزر arious arious ، روح Mو roperties P**

- **تضيف الواجهة Aspose.ThreeD. الكيانات. IMeshConvertible.** 
  - Any class that implements this interface can be converted to mesh while exporting to any 3D file formats.
- **يضيف فئة Aspose.ThreeD.Entities. Pritial.** 
-It مشتق من فئة Entity وأيضا الطبقة الأساسية لجميع الطبقات البدائية.
- **يضيف فئة Aspose.ThreeD.Entities.Box. Cylinder/Plane/Sphere/Torus.** 
-These يمكن استخدامها لتحديد المشهد مع البدائية بسيطة. Dإيفلين يمكن أيضا تحويلها إلى شبكة تلقائيا.

تشمل الأوليات العديد من الأشياء الأساسية والأكثر استخدامًا مثل الصندوق والكرة والطائرة والأسطوانة والطوف. يمكن للمطورين أيضًا تحويلها إلى شبكة لأغراض التعديل. توضح موضوعات المساعدة هذه كيفية القيام بذلك: [Convert ririmitive إلى Msh](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) و [Convert ririmitive إلى Msh](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex**
**يتم إضافة ليزر arious arious ، روح Mو roperties P**

- **يضيف فئة Aspose.ThreeD. الكيانات. TriMesh/TriMesh>** 
-Tريبليش/Tريبليش<T>يحتوي على تعريف الشبكات القائمة على المثلث مع تخطيط الذاكرة المخصصة ، وهو أمر مفيد عندما يتطلب المطور لتحويل المشهد إلى تنسيقات الملفات الخاصة بهم أو في تقديم.
- **يضيف هيكل Aspose.ThreeD. المرافق. FVector2/FVector3/FVector4** 
-هذه الفئات تعرض مكونات متجهة في الطفو. عدد قليل فقط من وحدة معالجة الرسوميةالحديثة تدعم ناقل الدقة المزدوج ، أنواع الطفو أحادية الدقة هي أكثر ترحيبا في عالم التقديم في الوقت الحقيقي. ستتواجد هذه البدائل مع Vector2/Vector3/Vector4 الأصلي لأنها تلعب أدوارًا مختلفة في Aspose.3D. تستخدم الدقة المزدوجة بشكل أساسي لتخزين بيانات النموذج لأنها تحتوي على خطأ متراكم أقل. يتم استخدام الدقة الأحادية بشكل أساسي في تحويل تنسيقات الملفات الخاصة بالمستخدم لأنها تتمتع بقبول وأداء أفضل. قدمنا هذه المجموعة من المتجهات بسعر Aspose.3D 1.5 لأننا أضفنا دعمًا لتخطيط قمة الرأس المخصص ، حيث سيتم استخدام المتجهات العائمة بشكل متكرر.
- **تضيف فئة السمات Aspose.ThreeD. Utility. Semanticسمة** 
-Dإيفلوبر يمكن تحديد هيكل مخصص ل فيرتكس ، واستخدام هذه السمة للاحتفال الدلالية من الحقول.
- **يضيف فئة Aspose.ThreeD. Utility. Vertexfarmit** 
-Describes t يصف تخطيط الذاكرة من قمة الرأس.
- **يضيف عدد Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
-أنواع These enum توضح نوع بيانات حقل فيرتكس والدلالية على التوالي.
- **يضيف فئة Aspose.ThreeD. Utility. VertexField** 
-Describes t يصف كل حقل في تخطيط الذاكرة المخصصة من erertex.
- **يضيف فئة Aspose.ThreeD. Upliciatures. Vertex** 
-يمكن استخدام It للوصول إلى القشرة الخام في TriMesh/TriMesh<T>

يمكن للمطورين تحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط الذاكرة المخصص للقمة. تعمل حزم برامج الرسوم والأجهزة بكفاءة أكبر على المثلثات. يوضح موضوع المساعدة هذا كيفية القيام بذلك: [Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
###  **Split esh sh**
**يتم إضافة ليزر arious arious ، روح Mو roperties P**

- **يضيف عدد Aspose.ThreeD. Quanites. SplitMeshPolicy** 
-It يحدد سياسة البيانات المستخدمة في خوارزمية تقسيم شبكة ، ونحن نؤيد اثنين من السياسات ، وتبادل البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها البيانات الخاصة بها (Oالبيانات المستخدمة nly).
- **تضيف 3 طرق سبليت شبكية إلى Aspose.ThreeD. Enability. فئة بوليجونموفيفير** 
1. hes تنسجم plit على عقدة محددة إلى شبكات فرعية حسب تعريف المواد.
1. Split كل شبكة في المشهد معين إلى الشبكات الفرعية حسب تعريف المواد.
1. pplit شبكة معينة إلى الشبكات الفرعية حسب تعريف المواد.
- **يضيف خاصية flipodrunatesystem في الفئة Aspose.ThreeD. Fults. Universal3DConfig** 
-يسمح للمستخدمين بقلب نظام الإحداثيات U3D أثناء الاستيراد أو التصدير.

قد يحتاج المطورون إلى تقسيم الشبكة تلقائيًا بواسطة مادة ، بحيث تستخدم كل شبكة مادة واحدة فقط أو شبكة منقسمة عن طريق تحديد المادة. توضح موضوعات المساعدة هذه كيفية القيام بذلك: [Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) و [Split ll ll hes تنسجم من cencene cener ateraterial](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **Emoemoval من تنسيق Distreet3D.**
يتم وضع علامة تنسيق Distreet3Dكما عفا عليها الزمن بسبب موجة غير صحيحة.
###  **يضيف تنسيق Discreet3DS.**
Discreet3DS format has been introduced.
###  **يضيف خاصية flipodrunatesystem في الفئة Aspose.ThreeD. Fults. Universal3DConfig**
يسمح للمستخدمين بقلب نظام الإحداثيات U3D أثناء الاستيراد أو التصدير.
