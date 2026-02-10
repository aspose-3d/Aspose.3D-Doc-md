---
title: Добавить иерархию узлов и поделиться геометрическими данными сетки между несколькими узлами сцены 3D
type: docs
weight: 20
url: /ru/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java поддерживает построение иерархии узлов. Узел является базовым строительным блоком сцены 3D, а иерархия узлов определяет логическую структуру сцены 3D и обеспечивает видимый контент путем присоединения к узлам геометрии, источников света и камер.
---
##  **Добавить иерархию узлов в документе сцены 3D**
Aspose.3D for Java поддерживает построение иерархии узлов. `Node` является базовым строительным блоком сцены 3D, а иерархия узлов определяет логическую структуру сцены 3D и обеспечивает видимый контент путем присоединения к узлам геометрии, источников света и камер.
###  **Пример графов сцены**

В Aspose.3D каждый экземпляр `Node` может иметь несколько дочерних узлов, в этом примере мы создали узел с двумя кубическими узлами, если мы повернем корневой узел, все дочерние узлы также будут затронуты:

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
##  **Поделитесь данными геометрии Mesh между несколькими узлами**
Чтобы уменьшить потребность в памяти, один экземпляр класса `Mesh` может быть привязан к различным экземплярам класса `Node`. Предположим, что вам нужна система, в которой все кубики 3D кажутся неразличимыми, но вам требуется большое количество из них. Вы можете сэкономить память, сделав один объект Mesh при старте системы. В этот момент каждый раз, когда вам нужна другая форма, вы делаете другой объект Node, а затем указываете этот узел на один `Mesh`. Это называется инстанцирование. Aspose.3D for Java API позволяют выполнять инстансирование.
###  **Пример установки**
В таких играх, как RTS (стратегия в реальном времени), мы всегда можем увидеть несколько NPC (Non-Player Character) с одной и той же моделью 3D, возможно, в разных цветах, движок рендеринга обычно разделяет одни и те же данные геометрии сетки между разными NPC, этот метод называется Instancing.

{{% alert color="primary" %}} 

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как там рассказано](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Демонстрация кода примера:

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


В этом примере мы создали 3 кубических узла, которые имеют одну и ту же сетку, каждый из них имеет разный материал с разными цветами.
