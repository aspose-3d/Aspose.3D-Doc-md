---
title: 使用点云
type: docs
weight: 150
url: /zh/python-net/working-with-pointcloud/
description: Aspose.3D Python via .NET允许直接从Draco文件解码网格，而无需使用DracoFormat类的解码方法构建场景。
---
{{% alert color="primary" %}} 

19.7或更高版本支持此功能。

{{% /alert %}} 
# **解码网格**
Aspose.3D Python via .NET允许直接从Draco文件解码网格，而无需使用[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)类的[`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1)方法构建场景。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
# **编码网格**
Aspose.3D Python via .NET允许直接将球体网格编码为Draco文件，而无需使用[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)类的[`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2)方法构建场景。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
# **将球体编码为点云**
Python via .NET的Aspose.3D允许使用[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)类的[`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2)方法将球体网格编码为将文件Draco为点云。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
# **将网格编码为PLY**
Aspose.3D Python via .NET允许将网格直接编码为PLY文件，而无需使用[编码](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)方法[PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)类。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
# **从PLY解码网格**
Aspose.3D Python via .NET允许使用[`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)类的[`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1)方法从PLY文件解码网格/点云。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
# **作为PointCloud导出到PLY**
Aspose.3D Python via .NET允许使用[`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)类的[`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)方法将场景导出为PointCloud PLY。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
# **将3D场景导出为点云**
{{% alert color="primary" %}} 

19.8或更高版本支持此功能。

{{% /alert %}} 

Aspose.3D Python via .NET允许使用[`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions)类的[`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud)属性将3D场景导出为PointCloud。下面的代码片段显示了如何使用此功能:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
