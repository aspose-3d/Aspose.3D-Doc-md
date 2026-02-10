---
title: 三角网格
type: docs
weight: 20
url: /zh/java/triangulate-mesh/
description: Aspose.3D for Java API 支持三角网格，这对游戏行业很有用，因为三角形是GPU硬件支持的唯一受支持的图元 (非三角形数据在驱动程序级别进行三角化，这在实时渲染中效率低下)。
---
Aspose.3D for Java API 支持三角网格，这对游戏行业很有用，因为三角形是GPU硬件支持的唯一受支持的图元 (非三角形数据在驱动程序级别进行三角化，这在实时渲染中效率低下)。示例代码:

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




