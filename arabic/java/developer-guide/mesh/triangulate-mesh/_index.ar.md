---
title: شبكة مثلثة
type: docs
weight: 20
url: /ar/java/triangulate-mesh/
description: Aspose. يدعم 3D for Java API شبكة تثليث ، وهو أمر مفيد لصناعة الألعاب لأن المثلث هو البدائي الوحيد المدعوم الذي تدعمه أجهزة وحدة معالجة مركزية (البيانات غير المثلثة مثلثة على مستوى السائق ، وهو غير فعال في التقديم في الوقت الفعلي).
---
Aspose. يدعم 3D for Java API شبكة تثليث ، وهو أمر مفيد لصناعة الألعاب لأن المثلث هو البدائي الوحيد المدعوم الذي تدعمه أجهزة وحدة معالجة مركزية (البيانات غير المثلثة مثلثة على مستوى السائق ، وهو غير فعال في التقديم في الوقت الفعلي). رمز المثال:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
scene.open(MyDir + "document.fbx");
scene.getRootNode().accept(new NodeVisitor() {
    @Override
    public boolean call(Node node) {
        Mesh mesh = (Mesh)node.getEntity();
        if (mesh != null)
        {
            // Triangulate the mesh
            Mesh newMesh = PolygonModifier.triangulate(mesh);
            // Replace the old mesh
            node.setEntity(newMesh);
        }
        return true;
    }
});
MyDir = MyDir + RunExamples.getOutputFilePath("document.fbx");
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}




