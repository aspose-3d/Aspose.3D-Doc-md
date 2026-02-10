---
title: Working with PointCloud
type: docs
weight: 150
url: /net/working-with-pointcloud/
description: Aspose.3D for .NET allows decoding a mesh from a Draco file directly without building a scene using the Decode method of DracoFormat class.
---

{{% alert color="primary" %}} 

This feature is supported by version 19.7 or greater.

{{% /alert %}} 
# **Decode Mesh**
Aspose.3D for .NET allows decoding a mesh from a Draco file directly without building a scene using the [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) method of [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var pointCloud = (PointCloud)FileFormat.Draco.Decode("point_cloud_no_qp.drc");

{{< /highlight >}}
# **Encode Mesh**
Aspose.3D for .NET allows encoding a sphere mesh to a Draco file directly without building a scene using the [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) method of [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
# **Encode Sphere as PointCloud**
Aspose.3D for .NET allows encoding a sphere mesh to Draco file as a point cloud using the [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) method of [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() { PointCloud = true });

{{< /highlight >}}
# **Encode Mesh to PLY**
Aspose.3D for .NET allows encoding a mesh to PLY file directly without building a scene using the [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
# **Decode Mesh From PLY**
Aspose.3D for .NET allows decoding a mesh/point cloud from a PLY file using the [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) method of [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
# **Export to PLY as PointCloud**
Aspose.3D for .NET allows exporting a scene to PLY as PointCloud using the [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions() { PointCloud = true });


{{< /highlight >}}
# **Export 3D Scene as Point Cloud**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 

Aspose.3D for .NET allows exporting a 3D scene as PointCloud using [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) property of [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions) class. The following code snippet shows how to use this functionality:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var scene = new Scene(new Sphere());
scene.Save("Export3DSceneAsPointCloud.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
