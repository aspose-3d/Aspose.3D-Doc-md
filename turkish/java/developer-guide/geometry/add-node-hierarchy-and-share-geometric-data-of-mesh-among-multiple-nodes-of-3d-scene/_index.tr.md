---
title: Düğüm hiyerarşisini ekleyin ve 3D sahnesinin birden fazla düğümleri arasında örgü geometrik verilerini paylaşın
type: docs
weight: 20
url: /tr/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java has support of building a hierarchy of Nodes. The Node is basic building block of 3D scene and a hierarchy of nodes defines the logical structure of 3D scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
---
##  **Düğüm hiyerarşisini 3D sahne belgesine ekleyin**
Aspose.3D for Java has support of building a hierarchy of Nodes. The `Node` is basic building block of 3D scene and a hierarchy of nodes defines the logical structure of 3D scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
###  **Cene cene Graph ample xample**

Aspose.3D, her bir `Node` örneği birden fazla çocuk düğümüne sahip olabilir, bu örnekte, kök düğümünü döndürürsek, tüm çocuk düğümleri de etkilenir:

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
##  **Hare hare Mesh eoeometry ata ata ultiultiple Nodes arasında**
In order to diminish memory necessities, a single instance of `Mesh` Class can be bound to various instances of `Node` Class. Envision that you require a system where all 3D cubes seemed to be indistinguishable, however you required numerous a large number of them. You could spare memory by making one Mesh object when the system begins up. At that point, each time you required another shape, you make another Node object, then point that node to the one `Mesh`. This is called instancing. Aspose.3D for Java APIs allow to do instancing.
###  **Instancing örneği**
Rts (gerçek zamanlı strateji) oyunlarında, her zaman aynı 3D modeliyle birden fazla npcs (oyuncu olmayan karakter) görebiliriz, belki farklı renklerde, işleme motoru genellikle farklı npc'lerde aynı örgü geometri verilerini paylaşır, bu tekniğe anında denir.

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Örnek kodun stration emonstration:

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


In bu örnek biz 3 küp düğümleri aynı örgü paylaşmak, her biri farklı renklerde farklı malzeme var.
