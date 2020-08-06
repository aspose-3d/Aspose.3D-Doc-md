---
title: Merge Meshes in 3D file
type: docs
weight: 90
url: /net/merge-meshes-in-3d-file/
---

## **Merge Meshes into a single valid Mesh**
Developers can merge multiple meshes into a single valid mesh. They might convert all meshes of a 3D scene, a node or a set of nodes into a single mesh. In order to achieve this, there are three MergeMesh members in the Aspose.ThreeD.Entities.PolygonModifier class.

**Definition**

{{< highlight java >}}

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

The code sample below merge all meshes of a scene in a single valid mesh.

**C#**

{{< highlight java >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
