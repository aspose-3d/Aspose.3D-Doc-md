---
title: أضف التسلسل الهرمي للعقدة وشارك البيانات الهندسية للشبكة بين العقد المتعددة لمشهد 3D
type: docs
weight: 40
url: /ar/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET عروض لإنشاء تسلسل هرمي للعقدة. العقدة هي كتلة البناء الأساسية للمشهد. يحدد التسلسل الهرمي للعقد الهيكل المنطقي للمشهد ، ويوفر محتوى مرئيًا عن طريق إرفاق أشكال التعديل ، والأضواء ، والكاميرات بالعقد.
---
##  **أضف التسلسل الهرمي للعقدة في مستند مشهد 3D**
Aspose.3D for .NET عروض لإنشاء تسلسل هرمي للعقدة. العقدة هي كتلة البناء الأساسية للمشهد. يحدد التسلسل الهرمي للعقد الهيكل المنطقي للمشهد ، ويوفر محتوى مرئيًا عن طريق إرفاق أشكال التعديل ، والأضواء ، والكاميرات بالعقد.
###  **Sسين rapراب Example**
A نموذج المشهد التسلسل الهرمي يشبه:

! [Todo: image_ altttext](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

في Aspose.3D ، يمكن أن يكون لكل مثيل `Node` عقد أطفال متعددة ، في هذا المثال ، أنشأنا عقدة بها عقدتان مكعبتان ، وإذا قمنا بتدوير عقدة الجذر ، تتأثر جميع العقد التابعة أيضًا:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Get a child node object
Node top = scene.RootNode.CreateChildNode();
// Each cube node has their own translation
Node cube1 = top.CreateChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();            
// Point node to the mesh
cube1.Entity = mesh;
// Set first cube translation
cube1.Transform.Translation = new Vector3(-10, 0, 0);
Node cube2 = top.CreateChildNode("cube2");
// Point node to the mesh
cube2.Entity = mesh;
// Set second cube translation
cube2.Transform.Translation = new Vector3(10, 0, 0);

// The rotated top node will affect all child nodes
top.Transform.Rotation = Quaternion.FromEulerAngle(Math.PI, 4, 0);
          
// Save 3D scene in the supported file formats
scene.Save("NodeHierarchy.fbx");

{{< /highlight >}}
##  **Des hare esh sh's omeeometry ata ata بين oultiple oodes**
لتقليل ضروريات الذاكرة ، يمكن ربط مثيل واحد لفئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) بمثيلات مختلفة من فئة [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node). تصور أنك تحتاج إلى نظام حيث يبدو أن جميع مكعبات 3D لا يمكن تمييزها ، لكنك طلبت عددًا كبيرًا منها. يمكنك حفظ الذاكرة عن طريق صنع كائن شبكي واحد عندما يبدأ النظام. عند تلك النقطة ، في كل مرة تطلب فيها شكلاً آخر ، تصنع جسم عقدة آخر ، ثم تشير إلى تلك العقدة إلى شبكة واحدة. وهذا ما يسمى التثبيت. Aspose.3D for .NET APIs تسمح بالقيام بالتثبيت.
###  **مثال على ذلك**
في ألعاب RTS (استراتيجية الوقت الفعلي) مثل ، يمكننا دائمًا رؤية أجهزة NPCs متعددة (شخصية غير لاعب) بنفس الطراز 3D ، ربما بألوان مختلفة ، مما يجعل المحرك عادةً يشارك بيانات هندسة الشبكة نفسها عبر أجهزة NPCs مختلفة ، وتسمى هذه التقنية التثبيت.

{{% alert color="primary" %}}

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Emتوضيح رمز المثال:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Define color vectors
Vector3[] colors = new Vector3[] {
new Vector3(1, 0, 0),
new Vector3(0, 1, 0),
new Vector3(0, 0, 1)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
int idx = 0;
foreach (Vector3 color in colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.Entity = mesh;
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.DiffuseColor = color;
    // Set material
    cube.Material = mat;
    // Set translation
    cube.Transform.Translation = new Vector3(idx++ * 20, 0, 0);
    // Add cube node
    scene.RootNode.ChildNodes.Add(cube);
}
        
// Save 3D scene in the supported file formats
scene.Save("MeshGeometryData.fbx");

{{< /highlight >}}

In هذا المثال أنشأنا 3 العقد مكعب حصة نفس الشبكة ، كل واحد منهم لديها مواد مختلفة بألوان مختلفة.
