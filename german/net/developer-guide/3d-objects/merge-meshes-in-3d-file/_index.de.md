---
title: Meshes in der Datei 3D zusammenführen
type: docs
weight: 90
url: /de/net/merge-meshes-in-3d-file/
description: Entwickler können mehrere Netze zu einem einzigen gültigen Netz zusammenführen. Sie können alle Netze einer 3D-Szene, eines Knotens oder einer Gruppe von Knoten in ein einzelnes Netz konvertieren. Um dies zu erreichen, gibt es drei MergeMesh-Mitglieder in der Klasse Aspose.ThreeD.Entities.Polygon Modifier.
---
## **Meshes zu einem einzigen gültigen Netz zusammenführen**
Entwickler können mehrere Netze zu einem einzigen gültigen Netz zusammenführen. Sie können alle Netze einer 3D-Szene, eines Knotens oder einer Gruppe von Knoten in ein einzelnes Netz konvertieren. Um dies zu erreichen, gibt es in der Klasse `Aspose.ThreeD.Entities.PolygonModifier` drei `MergeMesh` Mitglieder.

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

Im folgenden Code beispiel werden alle Maschen einer Szene in einem einzigen gültigen Netz zusammen geführt.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
