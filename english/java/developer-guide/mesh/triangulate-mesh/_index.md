---
title: Triangulate Mesh
type: docs
weight: 20
url: /java/triangulate-mesh/
description: Aspose.3D for Java API has support of triangulating mesh, which is useful for game industry because the triangle is the only supported primitive that GPU hardware supports(non-triangle data are triangulated in driver-level, which is inefficient in real-time rendering). 
---

Aspose.3D for Java API has support of triangulating mesh, which is useful for game industry because the triangle is the only supported primitive that GPU hardware supports(non-triangle data are triangulated in driver-level, which is inefficient in real-time rendering). Example code:

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




