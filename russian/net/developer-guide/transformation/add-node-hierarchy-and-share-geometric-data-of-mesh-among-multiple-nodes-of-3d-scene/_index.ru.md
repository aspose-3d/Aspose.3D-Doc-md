---
title: Добавить иерархию узлов и поделиться геометрическими данными сетки между несколькими узлами сцены 3D
type: docs
weight: 40
url: /ru/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET предлагает построить иерархию узлов. Узел является основным строительным блоком сцены. Иерархия узлов определяет логическую структуру сцены и обеспечивает видимый контент путем присоединения к узлам геометрии, источников света и камер.
---
##  **Добавить иерархию узлов в документе сцены 3D**
Aspose.3D for .NET предлагает построить иерархию узлов. Узел является основным строительным блоком сцены. Иерархия узлов определяет логическую структуру сцены и обеспечивает видимый контент путем присоединения к узлам геометрии, источников света и камер.
###  **Пример графов сцены**
Образец иерархии сцен выглядит так:

! [Для: имаге_альт_текст](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

В Aspose.3D каждый экземпляр `Node` может иметь несколько дочерних узлов, в этом примере мы создали узел с двумя кубическими узлами, если мы повернем корневой узел, все дочерние узлы также будут затронуты:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Get a child node object
Node top = scene.RootNode.CreateChildNode();
// Each cube node has their own translation
Node cube1 = top.CreateChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();            
// Point node to the mesh
cube1.Entity = mesh;
// Set first cube translation
cube1.Transform.Translation = new Vector3(-10, 0, 0);
Node cube2 = top.CreateChildNode("cube2");
// Point node to the mesh
cube2.Entity = mesh;
// Set second cube translation
cube2.Transform.Translation = new Vector3(10, 0, 0);

// The rotated top node will affect all child nodes
top.Transform.Rotation = Quaternion.FromEulerAngle(Math.PI, 4, 0);
          
// Save 3D scene in the supported file formats
scene.Save("NodeHierarchy.fbx");

{{< /highlight >}}
##  **Поделитесь данными геометрии Mesh между несколькими узлами**
Чтобы уменьшить потребность в памяти, один экземпляр класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) может быть привязан к различным экземплярам класса [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node). Предположим, что вам нужна система, в которой все кубики 3D кажутся неразличимыми, но вам требуется большое количество из них. Вы можете сэкономить память, сделав один объект Mesh при старте системы. В этот момент каждый раз, когда вам требуется другая форма, вы делаете другой объект Node, а затем указываете этот узел на одну Mesh. Это называется инстанцирование. Aspose.3D for .NET API позволяют выполнять инстансирование.
###  **Пример установки**
В таких играх, как RTS (стратегия в реальном времени), мы всегда можем увидеть несколько NPC (Non-Player Character) с одной и той же моделью 3D, возможно, в разных цветах, движок рендеринга обычно разделяет одни и те же данные геометрии сетки между разными NPC, этот метод называется Instancing.

{{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как там рассказано](/3d/ru/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Демонстрация кода примера:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Define color vectors
Vector3[] colors = new Vector3[] {
new Vector3(1, 0, 0),
new Vector3(0, 1, 0),
new Vector3(0, 0, 1)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
int idx = 0;
foreach (Vector3 color in colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.Entity = mesh;
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.DiffuseColor = color;
    // Set material
    cube.Material = mat;
    // Set translation
    cube.Transform.Translation = new Vector3(idx++ * 20, 0, 0);
    // Add cube node
    scene.RootNode.ChildNodes.Add(cube);
}
        
// Save 3D scene in the supported file formats
scene.Save("MeshGeometryData.fbx");

{{< /highlight >}}

В этом примере мы создали 3 кубических узла, которые имеют одну и ту же сетку, каждый из них имеет разный материал с разными цветами.
