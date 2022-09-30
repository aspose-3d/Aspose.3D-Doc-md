---
title: 合并3D文件中的网格
type: docs
weight: 90
url: /zh/net/merge-meshes-in-3d-file/
description: 开发人员可以将多个网格合并为一个有效网格。它们可以将3D场景、节点或一组节点的所有网格转换为单个网格。为了实现这一点，在Aspose.ThreeD.Entities.PolygonModifier类中有三个MergeMesh成员。
---
## **将网格合并为单个有效网格**
开发人员可以将多个网格合并为一个有效网格。它们可以将3D场景、节点或一组节点的所有网格转换为单个网格。为了实现这一点，`Aspose.ThreeD.Entities.PolygonModifier`类中有三个`MergeMesh`成员。

**定义**

{{< highlight "java" >}}

 // Convert a whole node to a single transformed mesh

// Vertex elements like normal/texture coordinates are not supported yet

// <param name="node">The node to merge</param>

// <returns>Merged mesh</returns>

public static Mesh MergeMesh(Node node)

// Convert a whole scene to a single transformed mesh

// Vertex elements like normal/texture coordinates are not supported yet

// <param name="scene">The scene to merge</param>

// <returns>The merged mesh</returns>

public static Mesh MergeMesh(Scene scene);

// Convert a set of nodes to a single transformed mesh

// Vertex elements like normal/texture coordinates are not supported yet

// <param name="nodes">The nodes to merge</param>

// <returns>Merged mesh</returns>

public static Mesh MergeMesh(IList<Node> nodes);

{{< /highlight >}}

下面的代码示例将场景的所有网格合并到单个有效网格中。

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
