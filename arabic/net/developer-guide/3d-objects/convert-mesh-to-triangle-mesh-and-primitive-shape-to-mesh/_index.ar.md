---
title: Convert Msh إلى Triangle esh sh و ririmitive Shape إلى Mesh
type: docs
weight: 30
url: /ar/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API يسمح للمطورين بتحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للقمة. يتم تعريف تخطيط الذاكرة المخصصة للقمة باستخدام البنية أو ديناميكيا بواسطة فئة vertexdication في أمثلة التعليمات البرمجية.
---
##  **Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex**
يسمح [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API للمطورين بتحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للقمة. يتم تعريف تخطيط الذاكرة المخصص للقمة باستخدام البنية أو ديناميكيا بواسطة فئة [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) في أمثلة التعليمات البرمجية.

{{% alert color="primary" %}}

يخلق موضوع المساعدة هذا شبكات من الصندوق والكرة للحفاظ على الرمز شامل وقصير. يمكن للمطورين إنشاء شبكة يدويًا كما روى في موضوع المساعدة هذا: [إنشاء شبكة مكعبة 3D](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}

أمثلة ese hese تظهر كيفية:

- [Convert ere phere إلى ririangle esh sh مع تخطيط ذاكرة مخصص من القشرة (محددة في شاحنة S)](/3d/ar/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert ox ox إلى ririangle esh sh مع تخطيط ذاكرة مخصص من القشرة (محددة من قبل فئة eclaration erertexD)](/3d/ar/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convert Msh**
قد تتحول شبكة إيفلين Dإلى شبكة مثلث لأن أي هيكل معقد (سطح) يمكن أن يمثل حفنة من المثلثات. Tانه مثلث هو الهندسة الأكثر ذرية. Hhus يتم استخدامه كقاعدة لأي شيء تقريبا.
###  **Ccccess erertices من ririangle esh sh**
Dإيفليرز يمكن الوصول إلى نقاط الاتصال ، vertices الفعلية ، vertices قبل دمج والبايت الإجمالية من vertices في الذاكرة.

مثال elelow يحول phere إلى شبكة مثلث مع تخطيط ذاكرة مخصص.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
[StructLayout(LayoutKind.Sequential)]
struct MyVertex
{
    [Semantic(VertexFieldSemantic.Position)]
    FVector3 position;
    [Semantic(VertexFieldSemantic.Normal)]
    FVector3 normal;
}

public static void Run()
{
    // Initialize scene object
    Scene scene = new Scene();

    // Initialize Node class object
    Node cubeNode = new Node("sphere");

    Mesh sphere = (new Sphere()).ToMesh();
    // Convert any mesh into typed TriMesh
    var myMesh = TriMesh<MyVertex>.FromMesh(sphere);
    // Get the vertex data in customized vertex structure.
    MyVertex[] vertex = myMesh.VerticesToTypedArray();
    // Get the 32bit and 16bit indices
    int[] indices32bit;
    ushort[] indices16bit;
    myMesh.IndicesToArray(out indices32bit);
    myMesh.IndicesToArray(out indices16bit);
    using (MemoryStream ms = new MemoryStream())
    {
        // Or we can write the vertex directly into stream like:
        myMesh.WriteVerticesTo(ms);
        // The indice data can be directly write to stream, we support 32-bit and 16-bit indice.
        myMesh.Write16bIndicesTo(ms);
        myMesh.Write32bIndicesTo(ms);
    }
    // Point node to the Mesh geometry
    cubeNode.Entity = sphere;

    // Add Node to a scene
    scene.RootNode.ChildNodes.Add(cubeNode);

    // The path to the documents directory.
    string output = RunExamples.GetOutputFilePath("SphereToTriangleMeshCustomMemoryLayoutScene.fbx");

    // Save 3D scene in the supported file formats
    scene.Save(output, FileFormat.FBX7400ASCII);

    Console.WriteLine("Indices = {0}, Actual vertices = {1}, vertices before merging = {2}", myMesh.IndicesCount, myMesh.VerticesCount, myMesh.UnmergedVerticesCount);
    Console.WriteLine("Total bytes of vertices in memory {0}bytes", myMesh.VerticesSizeInBytes);
    Console.WriteLine("\n Converted a Sphere mesh to triangle mesh with custom memory layout of the vertex successfully.\nFile saved at " + output);
}

{{< /highlight >}}




مثال elelow يحول الثور Bإلى شبكة مثلث مع تخطيط ذاكرة مخصص.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Get mesh of the Box
Mesh box = (new Box()).ToMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.AddField(VertexFieldDataType.FVector4, VertexFieldSemantic.Position);
vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal);
// Get a triangle mesh
TriMesh triMesh = TriMesh.FromMesh(box);

{{< /highlight >}}
##  **Convert ririmitive إلى Msh**
باستخدام Aspose.3D for .NET ، يمكن للمطورين تحويل أي كائن بدائي إلى شبكة. تشمل الأوليات العديد من الأشياء الأساسية والأكثر استخدامًا مثل الصندوق والكرة والطائرة والأسطوانة والطوف.

{{% alert color="primary" %}}

يمكن تحويل أي فئة تقوم بتطبيق واجهة `IMeshConvertible` إلى شبكة أثناء التصدير إلى أي تنسيق ملفات 3D.

{{% /alert %}}
###  **Convert ere phere إلى Msh**
A المجال هو كائن هندسي مستدير تماما في الفضاء ثلاثي الأبعاد التي تظهر في كل مكان من الكرات الرياضية إلى الكواكب في الفضاء. استخدام et et priphere بدائية لإنشاء شبكة.
Tانه رمز المثال أدناه تحويل ere phere إلى شبكة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convert ox ox إلى Msh**
يصف ox ox ox مجموعة متنوعة من الحاويات والأوعية للاستخدام الدائم كتخزين ، أو للاستخدام المؤقت ، في كثير من الأحيان لنقل المحتويات. استخدام et et priox بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل الثور Bإلى شبكة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convert ممر Pإلى Msh**
طائرة تمتد بلا حدود دون سمك. مثال على الطائرة هو طائرة تنسيق. يتيح استخدام `Plane` البدائي لإنشاء شبكة. يحول مثال الرمز أدناه `Plane` إلى `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convert Cيندر إلى Msh**
اسطوانة A هي واحدة من الأشكال الهندسية المنحنية الأساسية ، والسطح الذي شكلتها النقاط على مسافة ثابتة من خط مستقيم معين ، محور الاسطوانة. It يمكن استخدامها في العديد من الأماكن ، على سبيل المثال كعمود أمام المنزل أو كسيارة driveshaft. Ets ets استخدام priيليندر بدائية لخلق شبكة. Tهو رمز المثال أدناه تحويل ylinder Cإلى شبكة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convert Torus إلى Msh**
A torus هو سطح الثورة الناتجة عن دوار دائرة في الفضاء ثلاثي الأبعاد حول محور متوافق مع الدائرة. If محور الثورة لا تلمس الدائرة ، والسطح لديه شكل حلقة ويسمى توروس الثورة. استخدام et et Torus بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل ororus إلى شبكة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
