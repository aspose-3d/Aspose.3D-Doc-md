---
title: Triangulate mesh
type: docs
weight: 20
url: /tr/java/triangulate-mesh/
description: Aspose.3D for Java API, oyun endüstrisi için yararlı olan triangulating mesh desteğine sahiptir, çünkü üçgen, gpu donanımının desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, sürücü seviyesinde triangulated edilir, bu gerçek zamanlı olarak verimsizdir).
---
Aspose.3D for Java API, oyun endüstrisi için yararlı olan triangulating mesh desteğine sahiptir, çünkü üçgen, gpu donanımının desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, sürücü seviyesinde triangulated edilir, bu gerçek zamanlı olarak verimsizdir). Örnek kod:

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




