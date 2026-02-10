---
title: 使用点云
type: docs
weight: 110
url: /zh/java/working-with-pointcloud/
description: Aspose.3D for Java 允许直接从 Draco 文件解码网格，而无需使用DracoFormat类的decode方法构建场景。
---
#  **解码网格**
Aspose.3D for Java 允许直接从 Draco 文件解码网格，而无需使用 [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) 类的 [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) 方法构建场景。以下代码段显示了如何使用此功能:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PointCloud pointCloud = (PointCloud) FileFormat.DRACO.decode(RunExamples.getDataDir() + "point_cloud_no_qp.drc");

{{< /highlight >}}
#  **编码网格**
Aspose.3D for Java 允许直接将球体网格编码为 Draco 文件，而无需使用 [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) 方法构建场景。以下代码段显示了如何使用此功能:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir() + "sphere.drc");

{{< /highlight >}}
#  **将球体编码为点云**
Aspose.3D for Java 允许使用 [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) 方法将球体网格编码为 Draco 文件作为点云。以下代码段显示了如何使用此功能:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
DracoSaveOptions opt = new DracoSaveOptions();
opt.setPointCloud(true);
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir()+"sphere.drc", opt);

{{< /highlight >}}
#  **将网格编码到 PLY**
Aspose.3D for Java 允许直接将网格编码为 PLY 文件，而无需使用 [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) 方法构建场景。以下代码段显示了如何使用此功能:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **从 PLY 解码网格**
Aspose.3D for Java 允许使用 [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) 类的 [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) 方法从 PLY 文件解码网格/点云。以下代码段显示了如何使用此功能:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **作为PointCloud导出到 PLY**
Aspose.3D for Java 允许使用 [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) 方法将场景作为PointCloud导出到 PLY。以下代码段显示了如何使用此功能:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PlySaveOptions opt = new PlySaveOptions();
opt.setPointCloud(true);
FileFormat.PLY.encode(new Sphere(),RunExamples.getDataDir() + "sphere.ply", opt);

{{< /highlight >}}
#  **将 3D 场景导出为点云**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 

Aspose.3D for Java 允许使用 [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions) 类的 [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) 方法将 3D 场景导出为PointCloud。以下代码段显示了如何使用此功能:

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
