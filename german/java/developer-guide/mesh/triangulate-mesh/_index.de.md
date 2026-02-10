---
title: Triangulate Mesh
type: docs
weight: 20
url: /de/java/triangulate-mesh/
description: Aspose.3D for Java API unterstützt das Triangulation snetz, was für die Spiele industrie nützlich ist, da das Dreieck das einzige unterstützte Primitiv ist, das die GPU-Hardware unterstützt (Nicht-Dreiecks-Daten werden auf Treiber ebene trianguliert, was in Echtzeit ineffizient ist-Time Rendering).
---
Aspose.3D for Java API unterstützt das Triangulation snetz, was für die Spiele industrie nützlich ist, da das Dreieck das einzige unterstützte Primitiv ist, das die GPU-Hardware unterstützt (Nicht-Dreiecks-Daten werden auf Treiber ebene trianguliert, was in Echtzeit ineffizient ist-Time Rendering). Beispiel code:

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




