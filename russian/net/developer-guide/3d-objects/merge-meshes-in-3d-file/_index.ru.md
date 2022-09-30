---
title: Объединение сеток в файле 3D
type: docs
weight: 90
url: /ru/net/merge-meshes-in-3d-file/
description: Разработчики могут объединять несколько сеток в одну действительную сетку. Они могут преобразовывать все сетки сцены 3D, узла или набора узлов в единую сетку. Для этого в классе Aspose.ThreeD.Entities.PolygonModifier есть три члена MergeMesh.
---
## **Объединение сетки в единую действительную сетку**
Разработчики могут объединять несколько сеток в одну действительную сетку. Они могут преобразовывать все сетки сцены 3D, узла или набора узлов в единую сетку. Для этого в классе `Aspose.ThreeD.Entities.PolygonModifier` есть три члена `Aspose.ThreeD.Entities.PolygonModifier`.

**Определение**

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

В приведенном ниже образце кода объединяются все сетки сцены в одной действительной сетке.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
