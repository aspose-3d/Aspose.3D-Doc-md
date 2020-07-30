---
title : "Aspose.3D for .NET 19.8 Release Notes" 
description : "" 
weight : 12105 
toc : false
type: docs
url: /net/releasenotes/2019/aspose.3d+for+.net+19.8+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 19.8 Release Notes


This page contains release notes for [Aspose.3D for .NET 19.8](https://docs2.aspose.com/3d/net/releasenotes/2019/aspose.3d+for+.net+19.8+release+notes)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-528|Add point cloud support in Wavefront OBJ |New Feature|
|THREEDNET-531|Security review of Aspose.3D|Enhancement|
|THREEDNET-536 |DRC to STL conversion failure|Bug|
|THREEDNET-537|Problem converting PLY to GLB|Bug|
|THREEDNET-539|The large point cloud may generate incorrect data|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### Added new property **PointCloud** in class Aspose.ThreeD.Formats.ObjSaveOptions

{{< code lang="cs" >}}
/// <summary>
/// Gets or sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false
/// </summary>
public bool PointCloud
{
    get;set;
}
{{< /code >}}

Sample code to generate a point cloud of Sphere in obj format.

{{< code lang="cs" >}}
var scene = new Scene(new Sphere());
scene.Save(@"sphere.obj", new ObjSaveOptions() { PointCloud = true });
{{< /code >}}

### Added new methods **CreatePolygon** Aspose.ThreeD.Entities.Mesh

{{< code lang="cs" >}}
/// <summary>
/// Create a polygon with 4 vertices(quad)
/// </summary>
/// <param name="v1">Index of the first vertex</param>
/// <param name="v2">Index of the second vertex</param>
/// <param name="v3">Index of the third vertex</param>
/// <param name="v4">Index of the fourth vertex</param>
public void CreatePolygon(int v1, int v2, int v3, int v4);
/// <summary>
/// Create a polygon with 3 vertices(triangle)
/// </summary>
/// <param name="v1">Index of the first vertex</param>
/// <param name="v2">Index of the second vertex</param>
/// <param name="v3">Index of the third vertex</param>
public void CreatePolygon(int v1, int v2, int v3);
{{< /code >}}

Sample code.

{{< code lang="cs" >}}
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.
{{< /code >}}

The newly added methods **CreatePolygon** allow you to create a triangle or quad without allocating extra memory, it's highly optimized internally.

### Removed old public field **PrettyPrint** in class Aspose.ThreeD.Formats.GLTFSaveOptions

This was removed and replaced by property with the same name, so legacy code that used this needs no modifications.

### Added new property **PrettyPrint** in class Aspose.ThreeD.Formats.GLTFSaveOptions

  

{{< code lang="cs" >}}
/// <summary>
/// The JSON content of GLTF file is indented for human reading, default value is false
/// </summary>
public bool PrettyPrint { get; set; }
{{< /code >}}

The old **PrettyPrint** was a public field, and it's been replaced by property for consistent.

