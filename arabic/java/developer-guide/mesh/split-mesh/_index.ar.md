---
title: Split esh sh
type: docs
weight: 10
url: /ar/java/split-mesh/
description: Aspose.3D for Java API يدعم تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. لن تقسم طريقة SplitMesh شبكة من المشهد ، إذا تم تعيين مادة واحدة لها. يمكن تحقيق ذلك باستخدام Aspose.3D for Java API.
---
##  **Split جميع شبكات من Sسين cener aterالمواد**
Aspose.3D for Java API يدعم تقسيم جميع شبكات المشهد إلى عدة شبكات فرعية لكل مادة. لن تقسم طريقة SplitMesh شبكة من المشهد ، إذا تم تعيين مادة واحدة لها. يمكن تحقيق ذلك باستخدام Aspose.3D for Java API.

{{% alert color="primary" %}} 

يحدد عدد `SplitMeshPolicy` نهج البيانات المستخدم في خوارزمية تقسيم الشبكة ، وهو يدعم سياستين ، ومشاركة البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها بياناتها الخاصة (البيانات المستخدمة فقط).

{{% /alert %}} 

Tانه رمز عينة أدناه تقسيم كل تنسجم من مشهد لكل مادة. تشارك شبكة ach ach الفرعية نفس البيانات المباشرة وتختلف فقط في المؤشرات.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "test.fbx";
// Load a 3D file
Scene scene = new Scene(MyDir);
// Split all meshes
PolygonModifier.splitMesh(scene, SplitMeshPolicy.CLONE_DATA);
// Save file
MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("test-splitted.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Split esh sh عن طريق التحقق من المواد المضادة للأشعة فوق البنفسجية**
Aspose.3D for Java API يدعم تقسيم شبكة عن طريق تحديد المادة يدويًا. يقوم خيار الشبكة المنقسمة بإنشاء كائنات منفصلة وستستخدم كل شبكة فرعية مادة واحدة فقط.
###  **Split esh sh من ox ox**
يخلق موضوع المساعدة هذا شبكة من الصندوق للحفاظ على الرمز شامل وقصير. يمكن للمطورين إنشاء شبكة يدويًا كما روى في موضوع المساعدة هذا: [إنشاء شبكة مكعبة 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). علاوة على ذلك ، يتكون الصندوق من 6 طائرات وستصبح كل طائرة شبكة فرعية. العينة البرمجية أدناه تقسم شبكة بدائية عن طريق تحديد المادة يدويًا.

{{< highlight "java" >}}
// Create a mesh of box(A box is composed by 6 planes)
Mesh box = (new Box()).toMesh();
// Create a material element on this mesh
VertexElementMaterial mat = (VertexElementMaterial) box.createElement(VertexElementType.MATERIAL, MappingMode.POLYGON, ReferenceMode.INDEX);
// and specify different material index for each plane
mat.setIndices(new int[]{0, 1, 2, 3, 4, 5});
// Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
// We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
Mesh[] planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.CLONE_DATA);
mat.getIndices().clear();
mat.setIndices(new int[]{0, 0, 0, 1, 1, 1});
// Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
// We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.COMPACT_DATA);
{{< /highlight >}}
