---
title: أضف التسلسل الهرمي للعقدة وشارك البيانات الهندسية للشبكة بين العقد المتعددة لمشهد 3D
type: docs
weight: 20
url: /ar/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java يدعم إنشاء تسلسل هرمي للعقد. العقدة عبارة عن كتلة بناء أساسية لمشهد 3D ويحدد التسلسل الهرمي للعقد الهيكل المنطقي لمشهد 3D ، ويوفر محتوى مرئيًا عن طريق ربط أشكال الأعمال الزخرفية والأضواء والكاميرات بالعقد.
---
##  **أضف التسلسل الهرمي للعقدة في مستند مشهد 3D**
Aspose.3D for Java يدعم إنشاء تسلسل هرمي للعقد. `Node` هو كتلة بناء أساسية لمشهد 3D ويحدد التسلسل الهرمي للعقد الهيكل المنطقي لمشهد 3D ، ويوفر محتوى مرئيًا عن طريق ربط الأشكال المغناطيسية والأضواء والكاميرات بالعقد.
###  **Sسين rapراب Example**

في Aspose.3D ، يمكن أن يكون لكل مثيل `Node` عقد أطفال متعددة ، في هذا المثال ، أنشأنا عقدة بها عقدتان مكعبتان ، وإذا قمنا بتدوير عقدة الجذر ، تتأثر جميع العقد التابعة أيضًا:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node top = scene.getRootNode().createChildNode();
// Each cube node has their own translation
Node cube1 = top.createChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cube1.setEntity(mesh);
// Set first cube translation
cube1.getTransform().setTranslation(new Vector3(-10, 0, 0));
Node cube2 = top.createChildNode("cube2");
// Point node to the mesh
cube2.setEntity(mesh);
// Set second cube translation
cube2.getTransform().setTranslation(new Vector3(10, 0, 0));
// The rotated top node will affect all child nodes
top.getTransform().setRotation(Quaternion.fromEulerAngle(Math.PI, 4, 0));
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("NodeHierarchy.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Des hare esh sh's omeeometry ata ata بين oultiple oodes**
من أجل تقليل ضروريات الذاكرة ، يمكن ربط مثيل واحد لفئة `Mesh` بمثيلات مختلفة لفئة `Node`. تصور أنك تحتاج إلى نظام حيث يبدو أن جميع مكعبات 3D لا يمكن تمييزها ، لكنك طلبت عددًا كبيرًا منها. يمكنك حفظ الذاكرة عن طريق صنع كائن شبكي واحد عندما يبدأ النظام. عند هذه النقطة ، في كل مرة تطلب فيها شكلاً آخر ، تقوم بإنشاء كائن عقدة آخر ، ثم تشير إلى تلك العقدة إلى `Mesh`. وهذا ما يسمى التثبيت. Aspose.3D for Java APIs تسمح بإجراء التثبيت.
###  **مثال على ذلك**
في ألعاب RTS (استراتيجية الوقت الفعلي) مثل ، يمكننا دائمًا رؤية أجهزة NPCs متعددة (شخصية غير لاعب) بنفس الطراز 3D ، ربما بألوان مختلفة ، مما يجعل المحرك عادةً يشارك بيانات هندسة الشبكة نفسها عبر أجهزة NPCs مختلفة ، وتسمى هذه التقنية التثبيت.

{{% alert color="primary" %}} 

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Emتوضيح رمز المثال:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Define color vectors
Vector3[] colors = new Vector3[] {
    new Vector3(1, 0, 0),
    new Vector3(0, 1, 0),
    new Vector3(0, 0, 1)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
int idx = 0;
for(Vector3 color : colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.setEntity(mesh);
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.setDiffuseColor(color);
    // Set material
    cube.setMaterial(mat);
    // Set translation
    cube.getTransform().setTranslation(new Vector3(idx++ * 20, 0, 0));
    // Add cube node
    scene.getRootNode().addChildNode(cube);
}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("MeshGeometryData.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


In هذا المثال أنشأنا 3 العقد مكعب حصة نفس الشبكة ، كل واحد منهم لديها مواد مختلفة بألوان مختلفة.
