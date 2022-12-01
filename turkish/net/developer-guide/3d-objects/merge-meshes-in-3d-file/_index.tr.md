---
title: M07M3D dosyasında eshes
type: docs
weight: 90
url: /tr/net/merge-meshes-in-3d-file/
description: Developers, birden fazla mesh'i tek bir geçerli ağa birleştirebilir. They, 3D sahnesinin, bir düğümün veya düğümlerin tümünü tek bir ağa dönüştürebilir. In bunu başarmak için, Aspose.ThreeD.Entities. olyolygon. odifier sınıfında üç MergeMesh üyesi vardır.
---
## **Mvalid tek bir geçerli Mesh içine eshes**
Developers, birden fazla mesh'i tek bir geçerli ağa birleştirebilir. They, 3D sahnesinin, bir düğümün veya düğümlerin tümünü tek bir ağa dönüştürebilir. In bunu başarmak için, `Aspose.ThreeD.Entities.PolygonModifier` sınıfında üç `MergeMesh` üyesi vardır.

**Definition**

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

The kod örneği aşağıdaki bir sahnenin tüm meshlerini tek bir geçerli ağ içinde birleştirir.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
