---
title: Düğüm hiyerarşisini ekleyin ve 3D sahnesinin birden fazla düğümleri arasında örgü geometrik verilerini paylaşın
type: docs
weight: 40
url: /tr/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET bir düğüm hiyerarşisi oluşturmayı teklif eder. Düğüm, bir sahnenin temel yapı bloğudur. Düğümlerin bir hiyerarşi, bir sahnenin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
---
##  **Düğüm hiyerarşisini 3D sahne belgesine ekleyin**
Aspose.3D for .NET bir düğüm hiyerarşisi oluşturmayı teklif eder. Düğüm, bir sahnenin temel yapı bloğudur. Düğümlerin bir hiyerarşi, bir sahnenin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
###  **Cene cene Graph ample xample**
A örnek sahne hiyerarşi gibi görünüyor:

! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

Aspose.3D, her bir `Node` örneği birden fazla çocuk düğümüne sahip olabilir, bu örnekte, kök düğümünü döndürürsek, tüm çocuk düğümleri de etkilenir:

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
##  **Hare hare Mesh eoeometry ata ata ultiultiple Nodes arasında**
To diminish memory necessities, a single instance of [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class can be bound to various instances of [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Envision that you require a system where all 3D cubes seemed to be indistinguishable, however you required numerous a large number of them. You could spare memory by making one Mesh object when the system begins up. At that point, each time you required another shape, you make another Node object, then point that node to the one Mesh. This is called instancing. Aspose.3D for .NET APIs allow to do instancing.
###  **Instancing örneği**
Rts (gerçek zamanlı strateji) oyunlarında, her zaman aynı 3D modeliyle birden fazla npcs (oyuncu olmayan karakter) görebiliriz, belki farklı renklerde, işleme motoru genellikle farklı npc'lerde aynı örgü geometri verilerini paylaşır, bu tekniğe anında denir.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Örnek kodun stration emonstration:

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

In bu örnek biz 3 küp düğümleri aynı örgü paylaşmak, her biri farklı renklerde farklı malzeme var.
