---
title: Треугольная сетка
type: docs
weight: 20
url: /ru/java/triangulate-mesh/
description: Aspose.3D for Java API поддерживает триангулирующую сетку, которая полезна для игровой индустрии, потому что треугольник-единственный поддерживаемый примитив, который поддерживает аппаратное обеспечение GPU (данные без треугольника триангулируются на уровне драйверов, что неэффективно при рендеринге в реальном времени).
---
Aspose.3D for Java API поддерживает триангулирующую сетку, которая полезна для игровой индустрии, потому что треугольник-единственный поддерживаемый примитив, который поддерживает аппаратное обеспечение GPU (данные без треугольника триангулируются на уровне драйверов, что неэффективно при рендеринге в реальном времени). Пример кода:

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




