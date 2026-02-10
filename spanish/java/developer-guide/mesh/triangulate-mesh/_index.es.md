---
title: Malla triangular
type: docs
weight: 20
url: /es/java/triangulate-mesh/
description: Aspose.3D for Java API tiene soporte de malla triangular, que es útil para la industria de los juegos porque el triángulo es la única primitiva compatible que admite el hardware de la GPU (los datos no triangulares se triangulan en el nivel del controlador, que es ineficiente en la representación en tiempo real).
---
Aspose.3D for Java API tiene soporte de malla triangular, que es útil para la industria de los juegos porque el triángulo es la única primitiva compatible que admite el hardware de la GPU (los datos no triangulares se triangulan en el nivel del controlador, que es ineficiente en la representación en tiempo real). Código de ejemplo:

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




