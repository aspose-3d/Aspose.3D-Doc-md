---
title: Create 3D Mesh and Scene
type: docs
weight: 40
url: /java/create-3d-mesh-and-scene/
---

## **Create a 3D Cube Mesh**
A **Mesh** is defined by a set of control points and the many n-sided polygons as needed. This article explains how to define a **Mesh**.

In order to create a **Mesh** surface, we need to define control points and polygons as follows:

- [Define the Control Points](/3d/java/create-3d-mesh-and-scene-html/)
- [Create Polygons with PolygonBuilder Class](/3d/java/create-3d-mesh-and-scene-html/)
- [Create Polygons](/3d/java/create-3d-mesh-and-scene-html/)

Here’s an example to attach a Phong material to the cube node:
### **Define the Control Points**
A mesh is composed by a set of control points in space, and polygons to describe the mesh surface, to create a mesh, we need to define the control points:

{{% alert color="primary" %}} 

The control points of all geometries in Aspose.3D use homogeneous coordinate, so it’s Vector4 instead of Vector3 in the example code.

{{% /alert %}} 

**Example:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



### **Create Polygons**
The control points are not renderable, to make the cube visible, we need to define polygons in each side:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



### **Create Polygons with PolygonBuilder Class**
We can also define polygon by vertices with PolygonBuilder class:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Now it’s finished, to make the mesh visible, we need to prepare a node for it.
## **How to Triangulate a Mesh**
Triangulate mesh is useful for game industry because the triangular is the only supported primitive that GPU hardware supports (non-triangular data are triangulated in driver-level, which is inefficient in real-time rendering)

{{% alert color="primary" %}} 

In this version we only triangulated the polygons since it's required by 3ds file exporting, normals/uvs and other vertex elements are lost during this procedure, we can implement this in the future.

{{% /alert %}} 

In this example, we triangulate a Mesh by importing FBX file and saved it in FBX format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
## **Create a 3D Cube Scene**
This topic demonstrates how to add Mesh geometry to the 3D scene. The example code places a cube and save 3D scene in the supported file formats.
### **Create a Cube Node**
A node is invisible, but the geometry attached to the node can be rendered.

{{% alert color="primary" %}} 

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Example:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

NOTE: The entities attached to the root node are usually ignored in CAD/CAM softwares, so we need to create a new node to render the geometry.

{{% /alert %}}
