---
title: Working with PointCloud
type: docs
weight: 150
url: /python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET allows decoding a mesh from a Draco file directly without building a scene using the Decode method of DracoFormat class.
---

{{% alert color="primary" %}} 

This feature is supported by version 19.7 or greater.

{{% /alert %}} 
# **Decode Mesh**
Aspose.3D for Python via .NET allows decoding a mesh from a Draco file directly without building a scene using the [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/dracoformat/decode/methods/1) method of [`DracoFormat`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:

{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))
{{< /highlight >}}
# **Encode Mesh**
Aspose.3D for Python via .NET allows encoding a sphere mesh to Draco file directly without building a scene using the [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/dracoformat/encode/methods/2) method of [`DracoFormat`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")
{{< /highlight >}}
# **Encode Sphere as PointCloud**
Aspose.3D for Python via .NET allows encoding a sphere mesh to Draco file as a point cloud using the [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/dracoformat/encode/methods/2) method of [`DracoFormat`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")
{{< /highlight >}}
# **Encode Mesh to PLY**
Aspose.3D for Python via .NET allows encoding a mesh to PLY file directly without building a scene using the [Encode](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [PlyFormat ](https://reference.aspose.com/python-net/3d/aspose.threed.formats/plyformat)class. The following code snippet shows how to use this functionality:

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply")
{{< /highlight >}}
# **Decode Mesh From PLY**
Aspose.3D for Python via .NET allows decoding a mesh/point cloud from a PLY file using the [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) method of [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) class. The following code snippet shows how to use this functionality:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
# **Export to PLY as PointCloud**
Aspose.3D for Python via .NET allows exporting a scene to PLY as PointCloud using the [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) class. The following code snippet shows how to use this functionality:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import PlySaveOptions

options = PlySaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply", options)

{{< /highlight >}}
# **Export 3D Scene as Point Cloud**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 

Aspose.3D for Python via .NET allows exporting a 3D scene as PointCloud using [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) property of [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions) class. The following code snippet shows how to use this functionality:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import ObjSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
scene = Scene(Sphere())
options = ObjSaveOptions()
options.point_cloud = true 
scene.save("data-dir"  + "Export3DSceneAsPointCloud.obj", options)

{{< /highlight >}}
