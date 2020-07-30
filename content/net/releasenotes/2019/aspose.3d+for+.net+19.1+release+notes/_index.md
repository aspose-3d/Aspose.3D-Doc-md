---
title : "Aspose.3D for .NET 19.1 Release Notes" 
description : "" 
weight : 12112 
toc : false
type: docs
url: /net/releasenotes/2019/aspose.3d+for+.net+19.1+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 19.1 Release Notes


This page contains release notes for [Aspose.3D for .NET 19.1](https://www.nuget.org/packages/Aspose.3D/19.1.0)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-346|UV atlas algorithm|New Feature|
|THREEDNET-467|AMF Exporter|New Feature|
|THREEDNET-469|Archive-based file format detection |New Feature|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added class Aspose.ThreeD.Formats.AMFSaveOptions

{{< code lang="cs" >}}
    /// <summary>
    /// Save options for AMF
    /// </summary>
    public class AMFSaveOptions : SaveOptions
    {
        /// <summary>
        /// Whether to use compression to reduce the final file size, default value is true
        /// </summary>
        public bool EnableCompression { get; set; }
    }
{{< /code >}}

#### New member added to the class Aspose.ThreeD.Entities.PolygonModifier：

{{< code lang="cs" >}}
        /// <summary>
        /// Generate UV data from the given input mesh and specified normal data.
        /// </summary>
        /// <param name="mesh">The input mesh</param>
        /// <param name="normals">The normal data</param>
        /// <returns>Generated UV data</returns>
        public static VertexElementUV GenerateUV(Mesh mesh, VertexElementNormal normals);
        /// <summary>
        /// Generate UV data from the given input mesh
        /// </summary>
        /// <param name="mesh">The input mesh</param>
        /// <returns>Generated UV data</returns>
        public static VertexElementUV GenerateUV(Mesh mesh);
{{< /code >}}

