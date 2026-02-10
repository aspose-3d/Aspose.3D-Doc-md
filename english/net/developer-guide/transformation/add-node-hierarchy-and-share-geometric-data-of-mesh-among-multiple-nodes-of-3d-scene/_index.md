---
title: Add Node hierarchy and Share Geometric data of Mesh among Multiple Nodes of 3D Scene
type: docs
weight: 40
url: /net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET offers to build a Node hierarchy. The Node is basic building block of a scene. A hierarchy of nodes defines the logical structure of a scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
---

## **Add Node Hierarchy in 3D Scene Document**
Aspose.3D for .NET offers to build a Node hierarchy. The Node is basic building block of a scene. A hierarchy of nodes defines the logical structure of a scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
### **Scene Graph Example**
A sample scene hierarchy looks like:

![todo:image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

In Aspose.3D, each `Node` instance can have multiple child nodes, in this example, we created a node with two cube nodes, if we rotate the root node, all child nodes are also get affected:

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
## **Share Mesh’s Geometry Data between Multiple Nodes**
To diminish memory necessities, a single instance of [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class can be bound to various instances of [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Envision that you require a system where all 3D cubes seemed to be indistinguishable, however you required numerous a large number of them. You could spare memory by making one Mesh object when the system begins up. At that point, each time you required another shape, you make another Node object, then point that node to the one Mesh. This is called instancing. Aspose.3D for .NET APIs allow to do instancing.
### **Instancing example**
In the RTS (Real-time strategy) games like, we can always see multiple NPCs (Non-Player Character) with same 3D model, maybe in different colors, rendering engine usually share same mesh geometry data across different NPCs, this technique is called Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demonstration of the example code:

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

In this example we created 3 cube nodes share the same mesh, each of them have different material with different colors.
