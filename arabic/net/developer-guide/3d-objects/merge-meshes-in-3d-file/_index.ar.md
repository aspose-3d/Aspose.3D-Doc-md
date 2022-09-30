---
title: في 3D ملف
type: docs
weight: 90
url: /ar/net/merge-meshes-in-3d-file/
description: يمكن opers إيفلين دمج شبكات متعددة في شبكة صالحة واحدة. Tيا قد تحول كل تنسجم من مشهد 3D ، عقدة أو مجموعة من العقد في شبكة واحدة. In من أجل تحقيق ذلك ، هناك ثلاثة أعضاء erergeMsh في فئة Aspose.ThreeD.
---
## **Merge ينسجم في واحد صالح Msh**
يمكن opers إيفلين دمج شبكات متعددة في شبكة صالحة واحدة. Tيا قد تحول كل تنسجم من مشهد 3D ، عقدة أو مجموعة من العقد في شبكة واحدة. من أجل تحقيق ذلك ، هناك ثلاثة أعضاء `MergeMesh` في فئة `Aspose.ThreeD.Entities.PolygonModifier`.

**إعادة صياغة**

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

Tانه رمز عينة أدناه دمج جميع تنسجم المشهد في شبكة صالحة واحدة.

**C#**

{{< highlight "java" >}}

 // load a 3D scene

Scene scene = new Scene("LAD-TOP.rvm");

// merge all meshes

Mesh mesh = PolygonModifier.MergeMesh(scene);

// encode this mesh into the PLY format

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
