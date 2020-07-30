---
title : "Aspose.3D for Java 19.7 Release Notes" 
description : "" 
weight : 12066 
toc : false
type: docs
url: /java/releasenotes/2019/aspose.3d+for+java+19.7+release+notes/
---

# Aspose.3D for Java : Aspose.3D for Java 19.7 Release Notes


This page contains release notes for [Aspose.3D for Java 19.7](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.7)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-449|Problem with transformation values in Nodes|Feature|
|THREEDNET-526|Add point cloud export support in Google Draco|Enhancement|
|THREEDNET-524|Add point cloud import support in Google Draco|Enhancement|
|THREEDNET-523 |Add point cloud support in PLY format |Enhancement|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### Added new class com.aspose.threed.PointCloud

This class inherits from Aspose.ThreeD.Entities.Geometry directly and used to represent a set of points.

### Added new methods decode to class com.aspose.threed.DracoFormat

{{< code lang="cs" >}}
 	/**
     * Decode the point cloud or mesh from specified file name
     * @param fileName The file name contains the drc file
     * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance depends on the file content
     */
    public Geometry decode(String fileName)
        throws ImportException;
    /**
     * Decode the point cloud or mesh from memory data
     * @param data The raw drc bytes
     * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance depends on the content
     */
    public Geometry decode(byte[] data)
        throws ImportException;
{{< /code >}}

Sample code to decode a mesh from a draco file directly without building a scene

PointCloud pointCloud = (PointCloud)FileFormat.DRACO.decode("pointCloud.drc");

### Added new methods encode to class com.aspose.threed.DracoFormat

 /\*\*     \* Encode the entity to specified stream     \* @param entity The entity to be encoded     \* @param stream The stream that encoded data will be written to     \* @param options Extra options for encoding the point cloud     \*/    public void encode(Entity entity, Stream stream, DracoSaveOptions options)        throws IOException;    /\*\*     \* Encode the entity to specified stream     \* @param entity The entity to be encoded     \* @param stream The stream that encoded data will be written to     \*/    public void encode(Entity entity, Stream stream)        throws IOException;    /\*\*     \* Encode the entity to specified file     \* @param entity The entity to be encoded     \* @param fileName The file name to be written     \*/    public void encode(Entity entity, String fileName)        throws IOException;    /\*\*     \* Encode the entity to Draco raw data     \* @param entity The entity to be encoded     \* @param options Extra options for encoding the point cloud     \* @return The encoded draco data represented in bytes     \*/    public byte\[\] encode(Entity entity, DracoSaveOptions options);    /\*\*     \* Encode the entity to Draco raw data     \* @param entity The entity to be encoded     \* @return The encoded draco data represented in bytes     \*/    public byte\[\] encode(Entity entity);

Sample code to encode a sphere mesh to draco file directly without building a scene

FileFormat.DRACO.encode(new Sphere(), "sphere.drc");

### Added new getter/setter getPointCloud/setPointCloud to class com.aspose.threed.DracoSaveOptions

/\*\* \* Export the scene as point cloud, default value is false. \*/public boolean getPointCloud();/\*\* \* Export the scene as point cloud, default value is false. \* @param value New value \*/public void setPointCloud(boolean value);

Sample code to encode a sphere mesh to draco file as a point cloud

DracoSaveOptions opt = new DracoSaveOptions();opt.setPointCloud(true);FileFormat.DRACO.encode(new Sphere(), "sphere.drc", opt);

### Added new methods encode to class com.aspose.threed.PlyFormat

/\*\* \* Encode the entity and save the result into the stream. \* @param entity The entity to encode \* @param stream The stream to write to, this method will not close this stream \* @param opt Save options \*/public void encode(Entity entity, Stream stream, PlySaveOptions opt)    throws IOException;/\*\* \* Encode the entity and save the result into the stream. \* @param entity The entity to encode \* @param stream The stream to write to, this method will not close this stream \*/public void encode(Entity entity, Stream stream)    throws IOException;/\*\* \* Encode the entity and save the result into an external file. \* @param entity The entity to encode \* @param fileName The file to write to \* @param opt Save options \*/public void encode(Entity entity, String fileName, PlySaveOptions opt)    throws IOException;/\*\* \* Encode the entity and save the result into an external file. \* @param entity The entity to encode \* @param fileName The file to write to \*/public void encode(Entity entity, String fileName)    throws IOException;

Sample code to encode a mesh to ply file directly without building a scene.

FileFormat.PLY.encode(new Sphere(), "sphere.ply");

### Added new methods decode to class com.aspose.threed.PlyFormat

/\*\* \* Decode a point cloud or mesh from the specified stream. \* @param fileName The input stream \* @param opt The load option of PLY format \* @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance \*/public Geometry decode(String fileName, PlyLoadOptions opt)    throws IOException;/\*\* \* Decode a point cloud or mesh from the specified stream. \* @param fileName The input stream \* @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance \*/public Geometry decode(String fileName)    throws IOException;/\*\* \* Decode a point cloud or mesh from the specified stream. \* @param stream The input stream \* @param opt The load option of PLY format \* @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance \*/public Geometry decode(Stream stream, PlyLoadOptions opt)    throws IOException;/\*\* \* Decode a point cloud or mesh from the specified stream. \* @param stream The input stream \* @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance \*/public Geometry decode(Stream stream)    throws IOException;

Sample code to decode a mesh/point cloud from a ply file:

Geometry geom = FileFormat.PLY.decode("sphere.ply");

### Added getter/setter getPointCloud and setPointCloud to class com.aspose.threed.PlySaveOptions

/\*\* \* Export the scene as point cloud, the default value is false. \*/public boolean getPointCloud();/\*\* \* Export the scene as point cloud, the default value is false. \* @param value New value \*/public void setPointCloud(boolean value);

Sample code to force export a scene to ply as point cloud 

PlySaveOptions opt = new PlySaveOptions();opt.setPointCloud(true);FileFormat.PLY.encode(new Sphere(), "sphere.ply", opt);

