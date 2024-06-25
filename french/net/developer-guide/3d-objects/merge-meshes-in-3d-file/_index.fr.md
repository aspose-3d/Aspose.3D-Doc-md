---
title: Fusionner les maillages dans le fichier 3D
type: docs
weight: 90
url: /fr/net/merge-meshes-in-3d-file/
description: Les développeurs peuvent fusionner plusieurs maillages en un seul maillage valide. Ils peuvent convertir tous les maillages d'une scène 3D, d'un nœud ou d'un ensemble de nœuds en un seul maillage. Pour ce faire, il y a trois membres MergeMesh dans la classe Aspose.ThreeD.Entities.PolygonModifier.
---
##  **Fusionner les mailles en un seul maillage valide**
Les développeurs peuvent fusionner plusieurs maillages en un seul maillage valide. Ils peuvent convertir tous les maillages d'une scène 3D, d'un nœud ou d'un ensemble de nœuds en un seul maillage. Pour ce faire, il y a trois membres `MergeMesh` dans la classe `Aspose.ThreeD.Entities.PolygonModifier`.

**Définition**

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

L'exemple de code ci-dessous fusionne tous les maillages d'une scène dans un seul maillage valide.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
