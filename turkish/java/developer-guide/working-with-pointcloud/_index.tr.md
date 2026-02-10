---
title: Loud orking ile loud ointloud loud
type: docs
weight: 110
url: /tr/java/working-with-pointcloud/
description: Aspose.3D for Java, dracoformat sınıfının kod çözme yöntemini kullanarak bir sahne oluşturmadan doğrudan bir Draco dosyasından bir ağın çözülmesine izin verir.
---
#  **Decode Mesh**
Aspose.3D for Java allows decoding a mesh from a Draco file directly without building a scene using the [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) method of [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PointCloud pointCloud = (PointCloud) FileFormat.DRACO.decode(RunExamples.getDataDir() + "point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Encode Mesh**
Aspose.3D for Java allows encoding a sphere mesh to a Draco file directly without building a scene using the [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) method of [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir() + "sphere.drc");

{{< /highlight >}}
#  **Encode loud phere as loud ointloud loud**
Aspose.3D for Java allows encoding a sphere mesh to Draco file as a point cloud using the [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) method of [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
DracoSaveOptions opt = new DracoSaveOptions();
opt.setPointCloud(true);
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir()+"sphere.drc", opt);

{{< /highlight >}}
#  **Örgüyü PLY olarak kodlayın**
Aspose.3D for Java allows encoding a mesh to PLY file directly without building a scene using the [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) method of [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Ağını PLY 'dan çöz**
Aspose.3D for Java allows decoding a mesh/point cloud from a PLY file using the [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) method of [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Export to PLY as PointCloud**
Aspose.3D for Java allows exporting a scene to PLY as PointCloud using the [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) method of [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) class. The following code snippet shows how to use this functionality:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PlySaveOptions opt = new PlySaveOptions();
opt.setPointCloud(true);
FileFormat.PLY.encode(new Sphere(),RunExamples.getDataDir() + "sphere.ply", opt);

{{< /highlight >}}
#  **Export 3D Scene as Point Cloud**
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 

Aspose.3D for Java allows exporting a 3D scene as PointCloud using [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) method of [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions) class. The following code snippet shows how to use this functionality:

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
