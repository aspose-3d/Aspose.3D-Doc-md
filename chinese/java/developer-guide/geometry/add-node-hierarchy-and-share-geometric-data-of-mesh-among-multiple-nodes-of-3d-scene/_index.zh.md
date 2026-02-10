---
title: 添加节点层次结构并在 3D 场景的多个节点之间共享网格的几何数据
type: docs
weight: 20
url: /zh/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java 支持构建节点层次结构。节点是 3D 场景的基本构建块，节点层次结构定义了 3D 场景的逻辑结构，并通过将几何图形、灯光和相机附加到节点来提供可见内容。
---
##  **在 3D 场景文档中添加节点层次结构**
Aspose.3D for Java 支持构建节点层次结构。`Node` 是 3D 场景的基本构建块，节点层次结构定义了 3D 场景的逻辑结构，并通过将几何图形、灯光和相机附加到节点来提供可见内容。
###  **场景图示例**

在 Aspose.3D 中，每个 `Node` 实例可以有多个子节点，在这个例子中，我们创建了一个有两个立方体节点的节点，如果我们旋转根节点，所有子节点也会受到影响:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node top = scene.getRootNode().createChildNode();
// Each cube node has their own translation
Node cube1 = top.createChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cube1.setEntity(mesh);
// Set first cube translation
cube1.getTransform().setTranslation(new Vector3(-10, 0, 0));
Node cube2 = top.createChildNode("cube2");
// Point node to the mesh
cube2.setEntity(mesh);
// Set second cube translation
cube2.getTransform().setTranslation(new Vector3(10, 0, 0));
// The rotated top node will affect all child nodes
top.getTransform().setRotation(Quaternion.fromEulerAngle(Math.PI, 4, 0));
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("NodeHierarchy.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **在多个节点之间共享网格的几何数据**
为了减少内存需求，可以将 `Mesh` 类的单个实例绑定到 `Node` 类的各种实例。设想您需要一个系统，其中所有 3D 立方体似乎都无法区分，但是您需要大量的立方体。您可以通过在系统开始时制作一个网格对象来节省内存。在这一点上，每次你需要另一个形状，你做另一个节点对象，然后将该节点指向一个 `Mesh`。这称为实例化。Aspose.3D for Java api允许执行实例化。
###  **实例化示例**
在RTS (实时策略) 游戏中，我们总是可以看到多个npc (非玩家角色) 具有相同的 3D 模型，可能是不同的颜色，渲染引擎通常在不同的npc之间共享相同的网格几何数据，这种技术称为实例化。

{{% alert color="primary" %}} 

代码中正在使用 `Mesh` 类对象。我们可以 [创建一个网格类对象，如在那里叙述](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene)。

{{% /alert %}} 

演示示例代码:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Define color vectors
Vector3[] colors = new Vector3[] {
    new Vector3(1, 0, 0),
    new Vector3(0, 1, 0),
    new Vector3(0, 0, 1)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
int idx = 0;
for(Vector3 color : colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.setEntity(mesh);
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.setDiffuseColor(color);
    // Set material
    cube.setMaterial(mat);
    // Set translation
    cube.getTransform().setTranslation(new Vector3(idx++ * 20, 0, 0));
    // Add cube node
    scene.getRootNode().addChildNode(cube);
}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("MeshGeometryData.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


在此示例中，我们创建了3个多维数据集节点共享相同的网格，每个节点具有不同的材质和不同的颜色。
