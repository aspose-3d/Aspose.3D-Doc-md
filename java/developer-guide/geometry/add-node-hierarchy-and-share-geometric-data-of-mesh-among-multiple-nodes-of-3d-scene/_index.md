---
title: Add Node hierarchy and Share Geometric data of Mesh among Multiple Nodes of 3D Scene
type: docs
weight: 20
url: /java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java has support of building a hierarchy of Nodes. The Node is basic building block of 3D scene and a hierarchy of nodes defines the logical structure of 3D scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
---

## **Add Node Hierarchy in 3D Scene Document**
Aspose.3D for Java has support of building a hierarchy of Nodes. The Node is basic building block of 3D scene and a hierarchy of nodes defines the logical structure of 3D scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
### **Scene Graph Example**

In Aspose.3D, each Node instance can have multiple child nodes, in this example, we created a node with two cube nodes, if we rotate the root node, all child nodes are also get affected:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **Share Mesh’s Geometry Data between Multiple Nodes**
In order to diminish memory necessities, a single instance of **Mesh** Class can be bound to various instances of **Node** Class. Envision that you require a system where all 3D cubes seemed to be indistinguishable, however you required numerous a large number of them. You could spare memory by making one Mesh object when the system begins up. At that point, each time you required another shape, you make another Node object, then point that node to the one Mesh. This is called instancing. Aspose.3D for Java APIs allow to do instancing.
### **Instancing example**
In the RTS (Real-time strategy) games like, we can always see multiple NPCs (Non-Player Character) with same 3D model, maybe in different colors, rendering engine usually share same mesh geometry data across different NPCs, this technique is called Instancing.

{{% alert color="primary" %}} 

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demonstration of the example code:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


In this example we created 3 cube nodes share the same mesh, each of them have different material with different colors.
