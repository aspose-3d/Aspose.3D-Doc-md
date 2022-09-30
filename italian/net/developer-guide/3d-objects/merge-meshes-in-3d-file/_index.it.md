---
title: Unisci le maglie nel file 3D
type: docs
weight: 90
url: /it/net/merge-meshes-in-3d-file/
description: Gli sviluppatori possono unire più mesh in un'unica mesh valida. Potrebbero convertire tutte le mesh di una scena 3D, un nodo o un insieme di nodi in una singola mesh. Per raggiungere questo obiettivo, ci sono tre membri MergeMesh nella classe Aspose.ThreeD.Entities.PolygonModifier.
---
## **Unisci le maglie in un'unica mesh valida**
Gli sviluppatori possono unire più mesh in un'unica mesh valida. Potrebbero convertire tutte le mesh di una scena 3D, un nodo o un insieme di nodi in una singola mesh. Per raggiungere questo obiettivo, ci sono tre `MergeMesh` membri nella classe `Aspose.ThreeD.Entities.PolygonModifier`.

**Definizione**

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

Il codice di esempio seguente unisce tutte le mesh di una scena in una singola mesh valida.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
