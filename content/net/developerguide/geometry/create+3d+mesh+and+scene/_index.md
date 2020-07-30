---
title : "Create 3D Mesh and Scene" 
description : "" 
weight : 12023 
toc : false
type: docs
url: /net/developerguide/geometry/create+3d+mesh+and+scene/
---

# Aspose.3D for .NET : Create 3D Mesh and Scene


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Create a 3D Cube Mesh](#create-a-3d-cube-mesh)
    *   1.1 [Define the Control Points](#define-the-control-points)
    *   1.2 [Create Polygons](#create-polygons)
    *   1.3 [Create Polygons with PolygonBuilder Class](#create-polygons-with-polygonbuilder-class)
*   2 [How to Triangulate a Mesh](#how-to-triangulate-a-mesh)
*   3 [Create a 3D Cube Scene](#create-a-3d-cube-scene)
    *   3.1 [Create a Cube Node](#create-a-cube-node)
{{< /panel >}}
 

 

## Create a 3D Cube Mesh

A [Mesh](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Entities_Mesh) is defined by a set of control points and the many n-sided polygons as needed. This article explains how to define a [Mesh](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Entities_Mesh).

In order to create a [Mesh](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Entities_Mesh) surface, we need to define control points and polygons as follows:

*   [Define the Control Points](https://docs2.aspose.com/3d/net/developerguide/geometry/create+3d+mesh+and+scene)
*   [Create Polygons with PolygonBuilder Class](https://docs2.aspose.com/3d/net/developerguide/geometry/create+3d+mesh+and+scene)
*   [Create Polygons](https://docs2.aspose.com/3d/net/developerguide/geometry/create+3d+mesh+and+scene)  
    

Here’s an example to attach a Phong material to the cube node:

### Define the Control Points

A mesh is composed by a set of control points in space, and polygons to describe the mesh surface, to create a mesh, we need to define the control points:

The control points of all geometries in Aspose.3D use homogeneous coordinate, so it’s Vector4 instead of Vector3 in the example code.

**Example:**

### Create Polygons

The control points are not renderable, to make the cube visible, we need to define polygons in each side:

### Create Polygons with PolygonBuilder Class

We can also define polygon by vertices with PolygonBuilder class:

Now it’s finished, to make the mesh visible, we need to prepare a node for it.

## How to Triangulate a Mesh

Triangulate mesh is useful for game industry because the triangular is the only supported primitive that GPU hardware supports (non-triangular data are triangulated in driver-level, which is inefficient in real-time rendering)

In this version we only triangulated the polygons since it's required by 3ds file exporting, normals/uvs and other vertex elements are lost during this procedure, we can implement this in the future.

In this example, we triangulate a Mesh by importing FBX file and saved it in FBX format.

## Create a 3D Cube Scene

This topic demonstrates how to add Mesh geometry to the 3D scene. The example code places a cube and save 3D scene in the supported file formats.

### Create a Cube Node

A node is invisible, but the geometry attached to the node can be rendered.

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](http://www.aspose.com/docs/display/3dnet/Create+a+3D+Cube+Mesh+and+Scene#Createa3DCubeMeshandScene-Createa3DCubeMesh).

**Example:**

NOTE: The entities attached to the root node are usually ignored in CAD/CAM softwares, so we need to create a new node to render the geometry.

