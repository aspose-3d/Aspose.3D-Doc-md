---
title: Aدينغ رانسفورميشن إلى oode
type: docs
weight: 30
url: /ar/net/adding-transformation-to-the-node/
description: تُستخدم TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، قدمنا تحويل فئة للوصول إليها بـ Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET عروض لتدوير الكائنات في مساحة 3D. هناك ثلاث طرق لتحديد دوران الكائن بمساحة 3D وزوايا Euler و Quaternion والمصفوفة المخصصة ، وكلها مدعومة بفئة [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

تُستخدم TSR (الترجمة/القياس/الدوران) بشكل شائع في سيناريو 3D ، وقدمنا فئة `Transform` للوصول إليها بـ Aspose.3D. وتشمل التحولات في التخلف:

- تصنيف:
- Calالترسبات
- Rأوتيشن
- Hear سماع رسم الخرائط
- رسم الخرائط

{{% alert color="primary" %}}

كائن الفئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Rotate بواسطة Quaternion**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
// Point node to the Mesh geometry
cubeNode.Entity = mesh;
// Set rotation
cubeNode.Transform.Rotation = Quaternion.FromRotation(new Vector3(0, 1, 0), new Vector3(0.3, 0.5, 0.1));            
// Set translation
cubeNode.Transform.Translation = new Vector3(0, 0, 20);            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            
   
// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
##  **Rotate بواسطة Euler ngngles**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
// Point node to the Mesh geometry
cubeNode.Entity = mesh;
// Euler angles
cubeNode.Transform.EulerAngles = new Vector3(0.3, 0.1, -0.5);            
// Set translation
cubeNode.Transform.Translation = new Vector3(0, 0, 20);            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            

// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
##  **Custom ranransformation atatrix**
We يمكن أيضا استخدام Matrix مباشرة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
// Point node to the Mesh geometry
cubeNode.Entity = mesh;
// Set custom translation matrix
cubeNode.Transform.TransformMatrix = new Matrix4(
1, -0.3, 0, 0,
0.4, 1, 0.3, 0,
0, 0, 1, 0,
0, 20, 0, 1
);        
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);            
   
// Save 3D scene in the supported file formats
scene.Save("TransformationToNode.fbx");

{{< /highlight >}}
