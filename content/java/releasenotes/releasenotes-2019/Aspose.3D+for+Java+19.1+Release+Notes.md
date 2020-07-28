+++
title = "Aspose.3D for Java 19.1 Release Notes" 
description = "" 
weight = 12072 
+++

Aspose.3D for Java : Aspose.3D for Java 19.1 Release Notes  

# Aspose.3D for Java : Aspose.3D for Java 19.1 Release Notes


This page contains release notes for Aspose.3D for Java 19.1.

## Improvements and Changes

{{< table style="table-striped" >}}
|Summary|Category|
|:----|:----|
|UV atlas algorithm|New Feature|
|AMF Exporter|New Feature|
|Archive-based file format detection |New Feature|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added class com.aspose.threed.AMFSaveOptions:

{{< code lang="cs" >}}
/**
 * Save options for AMF
 */
public class AMFSaveOptions extends SaveOptions
{ 
    
    /**
     * Whether to use compression to reduce the final file size, default value is true
     */
    public boolean getEnableCompression();
    
    /**
     * Whether to use compression to reduce the final file size, default value is true
     * @param value New value
     */
    public void setEnableCompression(boolean value);
}
{{< /code >}}

#### New member added to the class com.aspose.threed.PolygonModifier:

{{< code lang="cs" >}}
    /**
     * Generate UV data from the given input mesh and specified normal data.
     * @param mesh The input mesh
     * @param normals The normal data
     * @return Generated UV data
     */
    public static VertexElementUV generateUV(Mesh mesh, VertexElementNormal normals);
    /**
     * Generate UV data from the given input mesh
     * @param mesh The input mesh
     * @return Generated UV data
     */
    public static VertexElementUV generateUV(Mesh mesh);
{{< /code >}}

