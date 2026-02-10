---
title: Arbeta med PointCloudName
type: docs
weight: 110
url: /sv/java/working-with-pointcloud/
description: Aspose. 3D for Java tillåter avkodning av ett mesh från en Draco-fil direkt utan att bygga en scen med hjälp av filen avkodningsmetod för DracoFormat-klassen.
---
#  **Avkoda mask**
Aspose. 3D for Java tillåter avkodning av ett mesh från en Draco-fil direkt utan att bygga en scen med hjälp av filen [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) metod för [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PointCloud pointCloud = (PointCloud) FileFormat.DRACO.decode(RunExamples.getDataDir() + "point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Koda mesh**
Aspose. 3D for Java tillåter kodning av ett sfärsnät till en Draco-fil direkt utan att bygga en scen med användning av en scen. [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-)-metoden i [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klassen. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir() + "sphere.drc");

{{< /highlight >}}
#  **Koda sfären som PointCloudName**
Aspose. 3D for Java tillåter kodning av ett sfärsnät till filen Draco som ett punktmoln med [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) metod för [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
DracoSaveOptions opt = new DracoSaveOptions();
opt.setPointCloud(true);
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir()+"sphere.drc", opt);

{{< /highlight >}}
#  **Koda mesh till PLY.**
Aspose.3D for Java allows encoding a mesh to PLY file directly without building a scene using the [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) method of [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Avkoda mesh från PLY.**
Aspose. 3D for Java gör det möjligt att avkoda ett mesh/punkt moln från en PLY-fil med [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-)-metoden. för [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Exportera till PLY som PointCloud?**
Aspose. 3D for Java gör det möjligt att exportera en scen till PLY som PointCloud med [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-)-metoden för [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) klassen. .. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PlySaveOptions opt = new PlySaveOptions();
opt.setPointCloud(true);
FileFormat.PLY.encode(new Sphere(),RunExamples.getDataDir() + "sphere.ply", opt);

{{< /highlight >}}
#  **Exportera 3D Scene som punktmoln**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 

Aspose. 3D for Java tillåter export av en 3D scen som PointCloud med [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-)-metoden för [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize Scene
Scene scene = new Scene(new Sphere());
// Initialize  ObjSaveOptions
ObjSaveOptions opt = new ObjSaveOptions();
// To export 3D scene as point cloud setPointCould
opt.setPointCloud(true);
// Save
scene.save(RunExamples.getDataDir()+ "export3DSceneAsPointCloud.obj", opt);

{{< /highlight >}}
