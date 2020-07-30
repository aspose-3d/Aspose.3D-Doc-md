---
title : "Merge Meshes in 3D file" 
description : "" 
weight : 12047 
toc : false
type: docs
url: /net/developerguide/3dobjects/merge+meshes+in+3d+file/
---

# Aspose.3D for .NET : Merge Meshes in 3D file


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Merge Meshes into a single valid Mesh](#merge-meshes-into-a-single-valid-mesh)
{{< /panel >}}
 

 

## Merge Meshes into a single valid Mesh

Developers can merge multiple meshes into a single valid mesh. They might convert all meshes of a 3D scene, a node or a set of nodes into a single mesh. In order to achieve this, there are three MergeMesh members in the Aspose.ThreeD.Entities.PolygonModifier class.

**Definition**

{{< code lang="cs" >}}
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
{{< /code >}}

The code sample below merge all meshes of a scene in a single valid mesh.

**C#**

{{< code lang="c#" >}}
// load a 3D scene
Scene scene = new Scene("LAD-TOP.rvm");
// merge all meshes
Mesh mesh = PolygonModifier.MergeMesh(scene);
// encode this mesh into the PLY format
FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");
{{< /code >}}

