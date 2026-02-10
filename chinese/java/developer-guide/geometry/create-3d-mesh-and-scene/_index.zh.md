---
title: 创建 3D 网格和场景
type: docs
weight: 40
url: /zh/java/create-3d-mesh-and-scene/
description: 网格由一组控制点和根据需要的许多n边多边形定义。本文介绍了如何定义网格。
---
##  **创建 3D 立方体网格**
`Mesh` 由一组控制点和所需的许多n边多边形定义。本文介绍如何定义 `Mesh`。

为了创建 `Mesh` 曲面，我们需要定义控制点和多边形，如下所示:

- [定义控制点](/3d/zh/java/create-3d-mesh-and-scene-html/)
- [使用 PolygonBuilder 类创建多边形](/3d/zh/java/create-3d-mesh-and-scene-html/)
- [创建多边形](/3d/zh/java/create-3d-mesh-and-scene-html/)

以下是将Phong材质附加到多维数据集节点的示例:
###  **定义控制点**
网格由一组空间中的控制点组成，多边形用于描述网格表面，要创建网格，我们需要定义控制点:

{{% alert color="primary" %}} 

Aspose.3D 中所有几何图形的控制点都使用齐次坐标，因此在示例代码中是 `Vector4` 而不是 `Vector3`。

{{% /alert %}} 

**示例:**

{{< highlight "java" >}}
// Initialize control points
Vector4List controlPoints = new Vector4List(8);
controlPoints.add(new Vector4( -5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, -5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, -5.0, 1.0));
{{< /highlight >}}



###  **创建多边形**
控制点不可渲染，为了使立方体可见，我们需要在每一侧定义多边形:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.createPolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
mesh.createPolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
mesh.createPolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
mesh.createPolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.createPolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
mesh.createPolygon(new int[] { 3, 2, 6, 7 });
{{< /highlight >}}



###  **使用 PolygonBuilder 类创建多边形**
我们还可以通过 PolygonBuilder 类的顶点定义多边形:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Indices of the vertices per each polygon
int[] indices = new int[]
{
    0,1,2,3, // Front face (Z+)
    1,5,6,2, // Right side (X+)
    5,4,7,6, // Back face (Z-)
    4,0,3,7, // Left side (X-)
    0,4,5,1, // Bottom face (Y-)
    3,2,6,7 // Top face (Y+)
};
int vertexId = 0;
PolygonBuilder builder = new PolygonBuilder(mesh);
for (int face = 0; face < 6; face++)
{
    // Start defining a new polygon
    builder.begin();
    for (int v = 0; v < 4; v++)
        // The indice of vertice per each polygon
        builder.addVertex(indices[vertexId++]);
    // Finished one polygon
    builder.end();
}
{{< /highlight >}}

现在完成了，为了使网格可见，我们需要为它准备一个节点。
##  **如何三角剖分网格**
三角网格对于游戏行业很有用，因为三角形是GPU硬件支持的唯一受支持的基元 (非三角数据在驱动程序级别进行三角划分，在实时渲染中效率低下)

{{% alert color="primary" %}} 

在此版本中，我们仅对多边形进行了三角化，因为3ds文件导出需要它，在此过程中会丢失法线/uv和其他顶点元素，因此将来可以实现。

{{% /alert %}} 

在此示例中，我们通过导入 FBX 文件并将其保存为 FBX 格式来对网格进行三角化。

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
##  **创建 3D 多维数据集场景**
本主题演示如何将网格几何体添加到 3D 场景。示例代码放置一个多维数据集，并以支持的文件格式保存 3D 场景。
###  **创建多维数据集节点**
节点是不可见的，但是可以渲染附加到该节点的几何图形。

{{% alert color="primary" %}} 

代码中正在使用Mesh类对象。我们可以 [创建一个网格类对象，如在那里叙述](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh)。

{{% /alert %}} 

**示例:**

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("CubeScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}

{{% alert color="primary" %}} 

注意: 在 CAD/CAM软件中，通常会忽略附加到根节点的实体，因此我们需要创建一个新节点来渲染几何图形。

{{% /alert %}}
