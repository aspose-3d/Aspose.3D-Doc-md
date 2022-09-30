---
title: Convert Msh إلى Triangle esh sh و ririmitive Shape إلى Mesh
type: docs
weight: 30
url: /ar/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API يسمح للمطورين بتحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط ذاكرة مخصص لـ vertex. Tيتم تعريف تخطيط الذاكرة المخصصة من erertex باستخدام شاحنة Sأو بشكل حيوي من قبل فئة eclaration ertexDفي أمثلة التعليمات البرمجية.
---
## **Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API يسمح للمطورين لتحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للقمة. Tيتم تعريف تخطيط الذاكرة المخصصة من erertex باستخدام شاحنة Sأو بشكل حيوي من قبل فئة [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) في أمثلة التعليمات البرمجية.

{{% alert color="primary" %}}

Tموضوع مساعدته يخلق تنسجم من صندوق ومجال للحفاظ على رمز شامل وقصير. Dإيفليرز قد بناء شبكة يدويا كما روى في هذا الموضوع مساعدة:[Ate reate a 3D Cube esh esh](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}

أمثلة ese hese تظهر كيفية:

- [Convert ere phere إلى ririangle esh sh مع تخطيط ذاكرة مخصص من القشرة (محددة في شاحنة S)](/3d/ar/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert ox ox إلى ririangle esh sh مع تخطيط ذاكرة مخصص من القشرة (محددة من قبل فئة eclaration erertexD)](/3d/ar/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convert Msh**
قد تتحول شبكة إيفلين Dإلى شبكة مثلث لأن أي هيكل معقد (سطح) يمكن أن يمثل حفنة من المثلثات. Tانه مثلث هو الهندسة الأكثر ذرية. Hhus يتم استخدامه كقاعدة لأي شيء تقريبا.
### **Ccccess erertices من ririangle esh sh**
Dإيفليرز يمكن الوصول إلى نقاط الاتصال ، vertices الفعلية ، vertices قبل دمج والبايت الإجمالية من vertices في الذاكرة.

مثال elelow يحول phere إلى شبكة مثلث مع تخطيط ذاكرة مخصص.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.cs" >}}




مثال elelow يحول الثور Bإلى شبكة مثلث مع تخطيط ذاكرة مخصص.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.cs" >}}
## **Convert ririmitive إلى Msh**
Using Aspose.3D for .NET ، يمكن للمطورين تحويل أي كائن بدائي إلى شبكة. وتشمل ريميفيرس Pالعديد من الأشياء الأساسية والأكثر استخداما مثل صندوق ، المجال ، الطائرة ، اسطوانة ، و توروس.

{{% alert color="primary" %}}

يمكن تحويل فئة ny ny التي تنفذ واجهة `IMeshConvertible` إلى mesh أثناء التصدير إلى أي تنسيق ملف 3D.

{{% /alert %}}
### **Convert ere phere إلى Msh**
A المجال هو كائن هندسي مستدير تماما في الفضاء ثلاثي الأبعاد التي تظهر في كل مكان من الكرات الرياضية إلى الكواكب في الفضاء. استخدام et et priphere بدائية لإنشاء شبكة.
Tانه رمز المثال أدناه تحويل ere phere إلى شبكة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.cs" >}}
### **Convert ox ox إلى Msh**
يصف ox ox ox مجموعة متنوعة من الحاويات والأوعية للاستخدام الدائم كتخزين ، أو للاستخدام المؤقت ، في كثير من الأحيان لنقل المحتويات. استخدام et et priox بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل الثور Bإلى شبكة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.cs" >}}
### **Convert ممر Pإلى Msh**
طائرة A تمتد بلا حدود دون سمك. An مثال على طائرة هو طائرة التنسيق. تستخدم ets ets بدائية `Plane` لإنشاء شبكة. Tهو رمز المثال أدناه يحول `Plane` إلى `Mesh`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.cs" >}}
### **Convert Cيندر إلى Msh**
اسطوانة A هي واحدة من الأشكال الهندسية المنحنية الأساسية ، والسطح الذي شكلتها النقاط على مسافة ثابتة من خط مستقيم معين ، محور الاسطوانة. It يمكن استخدامها في العديد من الأماكن ، على سبيل المثال كعمود أمام المنزل أو كسيارة driveshaft. Ets ets استخدام priيليندر بدائية لخلق شبكة. Tهو رمز المثال أدناه تحويل ylinder Cإلى شبكة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.cs" >}}
### **Convert Torus إلى Msh**
A torus هو سطح الثورة الناتجة عن دوار دائرة في الفضاء ثلاثي الأبعاد حول محور متوافق مع الدائرة. If محور الثورة لا تلمس الدائرة ، والسطح لديه شكل حلقة ويسمى توروس الثورة. استخدام et et Torus بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل ororus إلى شبكة.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.cs" >}}
