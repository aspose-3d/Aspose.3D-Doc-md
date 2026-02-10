---
title: Triangulera mask
type: docs
weight: 20
url: /sv/java/triangulate-mesh/
description: Aspose. 3D for Java API har stöd för att triangulera mesh, vilket är användbart för spelindustrin eftersom triangeln är den enda primitiva som GPU hårdvara stöder (icke-triangeldata trianguleras i driver- Nivå, som är ineffektiv i realtids rendering.
---
Aspose. 3D for Java API har stöd för att triangulera mesh, vilket är användbart för spelindustrin eftersom triangeln är den enda primitiva som GPU hårdvara stöder (icke-triangeldata trianguleras i driver- Nivå, som är ineffektiv i realtids rendering. Exempelkod:

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




