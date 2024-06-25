---
title: Sammanfoga maskor i 3D file
type: docs
weight: 90
url: /sv/net/merge-meshes-in-3d-file/
description: Utvecklare kan slå ihop flera maskor till en enda giltig mask. De kan konvertera alla maskor i en 3D-scen, en nod eller en uppsättning noder till ett enda mesh. För att uppnå detta finns det tre MergeMesh medlemmar i Aspose. 3D. Enheter. PolygonModifier- klass.
---
##  **Sammanfoga maskor till en enda giltig mesh**
Utvecklare kan slå ihop flera maskor till en enda giltig mask. De kan konvertera alla maskor i en 3D-scen, en nod eller en uppsättning noder till ett enda mesh. För att uppnå detta finns det tre `MergeMesh` medlemmar i `Aspose.ThreeD.Entities.PolygonModifier` klassen.

**Definition:**

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

Kodprovet nedan sammanfogar alla maskor i en scen i ett enda giltigt maskor.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
