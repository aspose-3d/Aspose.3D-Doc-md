---
title: Convert Msh إلى Triangle esh sh و ririmitive Shape إلى Mesh
type: docs
weight: 20
url: /ar/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API يدعم تحويل الشبكة إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للرأس. يتم تعريف تخطيط الذاكرة المخصصة للرأس بشكل ديناميكي بواسطة فئة vertexdication في أمثلة التعليمات البرمجية.
---
##  **Convert esh sh إلى Triangle esh sh مع Custom ememory Layout من Vertex**
Aspose.3D for Java API يدعم تحويل الشبكة إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للرأس. يتم تعريف تخطيط الذاكرة المخصصة للرأس بشكل ديناميكي بواسطة فئة `VertexDeclaration` في أمثلة التعليمات البرمجية.

{{% alert color="primary" %}}

يخلق موضوع المساعدة هذا شبكات من الصندوق والكرة للحفاظ على الرمز شامل وقصير. يمكن للمطورين إنشاء شبكة يدويًا كما روى في موضوع المساعدة هذا: [إنشاء شبكة مكعبة 3D](/3d/ar/java/create-3d-mesh-and-scene/).

{{% /alert %}}

قد تتحول شبكة إيفلين Dإلى شبكة مثلث لأن أي هيكل معقد (سطح) يمكن أن يمثل حفنة من المثلثات. Tانه مثلث هو الهندسة الأكثر ذرية. Hhus يتم استخدامه كقاعدة لأي شيء تقريبا. Tله مثال رمز تحويل الثور Bإلى شبكة مثلث مع تخطيط الذاكرة المخصصة.



{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("box");
// Get mesh of the Box
Mesh box = (new Box()).toMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.addField(VertexFieldDataType.F_VECTOR4, VertexFieldSemantic.POSITION);
vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
// Get a triangle mesh
TriMesh triMesh = TriMesh.fromMesh(box);
// ExEnd:ConvertBoxMeshtoTriangleMeshCustomMemoryLayout
// Point node to the Mesh geometry
cubeNode.setEntity(box);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("BoxToTriangleMeshCustomMemoryLayoutScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Convert ririmitive ape hape إلى Msh**
Aspose.3D for Java API يدعم تحويل أي شكل بدائي إلى شبكة. تشمل الأشكال البدائية معظم الأشياء الأساسية والمستعملة مثل الصندوق والكرة والطائرة والأسطوانة والطوف.

{{% alert color="primary" %}}

يمكن تحويل أي فئة تقوم بتطبيق واجهة قابلة للتحويل إلى شبكة أثناء التصدير إلى أي تنسيق ملف 3D.

{{% /alert %}}
###  **Convert Sphere rimitive إلى Msh**
A المجال هو كائن هندسي مستدير تماما في الفضاء ثلاثي الأبعاد التي تظهر في كل مكان من الكرات الرياضية إلى الكواكب في الفضاء. استخدام et et priphere بدائية لإنشاء شبكة.
Tانه رمز المثال أدناه تحويل ere phere إلى شبكة.

{{< highlight "java" >}}
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
// Convert a Sphere to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convert ox ox إلى Msh**
يصف ox ox ox مجموعة متنوعة من الحاويات والأوعية للاستخدام الدائم كتخزين ، أو للاستخدام المؤقت ، في كثير من الأحيان لنقل المحتويات. استخدام et et priox بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل الثور Bإلى شبكة.

{{< highlight "java" >}}
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convert ممر Pإلى Msh**
طائرة A تمتد بلا حدود دون سمك. An مثال على طائرة هو طائرة التنسيق. تستخدم ets ets حارة Pبدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل حارة Pإلى شبكة.

{{< highlight "java" >}}
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
// Convert a Plane to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convert Cيندر إلى Msh**
اسطوانة A هي واحدة من الأشكال الهندسية المنحنية الأساسية ، والسطح الذي شكلتها النقاط على مسافة ثابتة من خط مستقيم معين ، محور الاسطوانة. It يمكن استخدامها في العديد من الأماكن ، على سبيل المثال كعمود أمام المنزل أو كسيارة driveshaft. Ets ets استخدام priيليندر بدائية لخلق شبكة. Tهو رمز المثال أدناه تحويل ylinder Cإلى شبكة.

{{< highlight "java" >}}
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
// Convert a Cylinder to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convert Torus إلى Msh**
A torus هو سطح الثورة الناتجة عن دوار دائرة في الفضاء ثلاثي الأبعاد حول محور متوافق مع الدائرة. If محور الثورة لا تلمس الدائرة ، والسطح لديه شكل حلقة ويسمى توروس الثورة. استخدام et et Torus بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل ororus إلى شبكة.

{{< highlight "java" >}}
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
// Convert a Torus to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
