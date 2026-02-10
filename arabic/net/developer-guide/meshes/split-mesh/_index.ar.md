---
title: Split esh sh
type: docs
weight: 100
url: /ar/net/split-mesh/
description: قد يحتاج المطورون إلى تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. لن تقوم طريقة SplitMesh بتقسيم شبكة من المشهد إذا تم تعيين مادة واحدة لها. يمكن للمطورين الآن تحقيق ذلك باستخدام Aspose.3D for .NET API.
---
##  **Split ll ll hes تنسجم من cencene cener ateraterial**
قد يحتاج المطورون إلى تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. لن تقوم طريقة SplitMesh بتقسيم شبكة من المشهد إذا تم تعيين مادة واحدة لها. يمكن للمطورين الآن تحقيق ذلك باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

يحدد عدد `SplitMeshPolicy` نهج البيانات المستخدم في خوارزمية تقسيم الشبكة ، وهو يدعم سياستين ، ومشاركة البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها بياناتها الخاصة (البيانات المستخدمة فقط).

{{% /alert %}}

Tانه رمز عينة أدناه تقسيم كل تنسجم من مشهد لكل مادة. تشارك شبكة ach ach الفرعية نفس البيانات المباشرة وتختلف فقط في المؤشرات.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
string input = RunExamples.GetDataFilePath("test.fbx");

// Load a 3D file
Scene scene = new Scene(input);
// Split all meshes
PolygonModifier.SplitMesh(scene, SplitMeshPolicy.CloneData);

// Save file
var output = RunExamples.GetOutputFilePath("test-splitted.fbx");
scene.Save(output, FileFormat.FBX7500ASCII);


{{< /highlight >}}
##  **Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية**
Aspose.3D for .NET API يسمح للمطورين بتقسيم الشبكة عن طريق تحديد المادة يدويًا. يقوم خيار الشبكة المنقسمة بإنشاء كائنات منفصلة وستستخدم كل شبكة فرعية مادة واحدة فقط.
###  **Split Msh من ox ox**
يخلق موضوع المساعدة هذا شبكة من الصندوق للحفاظ على الرمز شامل وقصير. يمكن للمطورين إنشاء شبكة يدويًا كما روى في موضوع المساعدة هذا: [إنشاء شبكة مكعبة 3D](/3d/ar/net/create-3d-mesh-and-scene/). علاوة على ذلك ، يتكون الصندوق من 6 طائرات وستصبح كل طائرة شبكة فرعية. عينة الكود أدناه تقسم شبكة بدائية عن طريق تحديد المادة يدويًا.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a mesh of box(A box is composed by 6 planes)
            Mesh box = (new Box()).ToMesh();
            // Create a material element on this mesh
            VertexElementMaterial mat = (VertexElementMaterial)box.CreateElement(VertexElementType.Material, MappingMode.Polygon, ReferenceMode.Index);
            // And specify different material index for each plane
            mat.Indices.AddRange(new int[] { 0, 1, 2, 3, 4, 5 });
            // Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
            // We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
            Mesh[] planes = PolygonModifier.SplitMesh(box, SplitMeshPolicy.CloneData);

            mat.Indices.Clear();
            mat.Indices.AddRange(new int[] { 0, 0, 0, 1, 1, 1 });
            // Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
            // We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
            planes = PolygonModifier.SplitMesh(box, SplitMeshPolicy.CompactData);


{{< /highlight >}}
