---
title: Arbeta med PointCloudName
type: docs
weight: 150
url: /sv/net/working-with-pointcloud/
description: Aspose. 3D for .NET tillåter avkodning av ett mesh från en Draco-fil direkt utan att bygga en scen med hjälp av filen Avkoda metod för DracoFormat klassen.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.7 eller större.

{{% /alert %}} 
#  **Avkoda mask**
Aspose. 3D for .NET tillåter avkodning av ett mesh från en Draco-fil direkt utan att bygga en scen med hjälp av filen [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) metod för [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var pointCloud = (PointCloud)FileFormat.Draco.Decode("point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Koda mesh**
Aspose. 3D for .NET tillåter kodning av ett sfärsnät till en Draco-fil direkt utan att bygga en scen med användning av en scen. [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2)-metoden i [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) klassen. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
#  **Koda sfären som PointCloudName**
Aspose. 3D for .NET tillåter kodning av ett sfärsnät till filen Draco som ett punktmoln med [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) metod för [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() { PointCloud = true });

{{< /highlight >}}
#  **Koda mesh till PLY.**
Aspose.3D for .NET allows encoding a mesh to PLY file directly without building a scene using the [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) class. The following code snippet shows how to use this functionality:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Avkoda mesh från PLY.**
Aspose. 3D for .NET gör det möjligt att avkoda ett mesh/punkt moln från en PLY-fil med [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1)-metoden. för [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Exportera till PLY som PointCloud?**
Aspose. 3D for .NET gör det möjligt att exportera en scen till PLY som PointCloud med [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1)-metoden för [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) klassen. .. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions() { PointCloud = true });


{{< /highlight >}}
#  **Exportera 3D Scene som punktmoln**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 

Aspose. 3D for .NET tillåter export av en 3D scen som PointCloud med egenskap [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) i klassen [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions) .. Följande kodsnutt visar hur denna funktionalitet ska användas:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var scene = new Scene(new Sphere());
scene.Save("Export3DSceneAsPointCloud.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
