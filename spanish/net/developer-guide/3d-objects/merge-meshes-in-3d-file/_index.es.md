---
title: Combinar mallas en el archivo 3D
type: docs
weight: 90
url: /es/net/merge-meshes-in-3d-file/
description: Los desarrolladores pueden combinar varias mallas en una sola malla válida. Podrían convertir todas las mallas de una escena 3D, un nodo o un conjunto de nodos en una sola malla. Para lograr esto, hay tres miembros de MergeMesh en la clase Aspose.ThreeD.Entities.PolygonModifier.
---
##  **Combinar mallas en una sola malla válida**
Los desarrolladores pueden combinar varias mallas en una sola malla válida. Podrían convertir todas las mallas de una escena 3D, un nodo o un conjunto de nodos en una sola malla. Para lograr esto, hay tres miembros `MergeMesh` en la clase `Aspose.ThreeD.Entities.PolygonModifier`.

**Definición**

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

El ejemplo de código a continuación combina todas las mallas de una escena en una única malla válida.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
