---
title: 使用点云
type: docs
weight: 110
url: /zh/java/working-with-pointcloud/
description: Aspose.3D for Java 允许直接从 Draco 文件解码网格，而无需使用DracoFormat类的decode方法构建场景。
---
#  **解码网格**
Aspose.3D for Java 允许直接从 Draco 文件解码网格，而无需使用 [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) 类的 [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) 方法构建场景。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
#  **编码网格**
Aspose.3D for Java 允许直接将球体网格编码为 Draco 文件，而无需使用 [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) 方法构建场景。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
#  **将球体编码为点云**
Aspose.3D for Java 允许使用 [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) 方法将球体网格编码为 Draco 文件作为点云。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
#  **将网格编码到 PLY**
Aspose.3D for Java 允许直接将网格编码为 PLY 文件，而无需使用 [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) 方法构建场景。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **从 PLY 解码网格**
Aspose.3D for Java 允许使用 [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) 类的 [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) 方法从 PLY 文件解码网格/点云。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **作为PointCloud导出到 PLY**
Aspose.3D for Java 允许使用 [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) 类的 [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) 方法将场景作为PointCloud导出到 PLY。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
#  **将 3D 场景导出为点云**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 

Aspose.3D for Java 允许使用 [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions) 类的 [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) 方法将 3D 场景导出为PointCloud。以下代码段显示了如何使用此功能:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
