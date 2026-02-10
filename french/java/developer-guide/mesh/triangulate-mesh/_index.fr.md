---
title: Maille triangulée
type: docs
weight: 20
url: /fr/java/triangulate-mesh/
description: Aspose.3D for Java API prend en charge le maillage de triangulation, ce qui est utile pour l'industrie du jeu car le triangle est la seule primitive supportée par le matériel GPU (les données non triangulées sont triangulées au niveau du pilote, ce qui est inefficace dans le rendu en temps réel).
---
Aspose.3D for Java API prend en charge le maillage de triangulation, ce qui est utile pour l'industrie du jeu car le triangle est la seule primitive supportée par le matériel GPU (les données non triangulées sont triangulées au niveau du pilote, ce qui est inefficace dans le rendu en temps réel). Exemple de code:

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




