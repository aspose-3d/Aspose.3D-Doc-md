---
title: Loud orking ile loud ointloud loud
type: docs
weight: 150
url: /tr/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET, dracoformat sınıfının kod çözme yöntemini kullanarak bir sahne oluşturmadan doğrudan bir Draco dosyasından bir ağın çözülmesine izin verir.
---
{{% alert color="primary" %}} 

This özelliği 19.7 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
#  **Decode Mesh**
Aspose.3D for Python via .NET, [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) sınıfının [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) yöntemini kullanarak bir sahne oluşturmadan doğrudan bir Draco dosyasından bir ağın çözülmesine izin verir. Aşağıdaki kod parçacığı, bu işlevselliğin nasıl kullanılacağını gösterir:



{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))

{{< /highlight >}}
#  **Encode Mesh**
Aspose.3D for Python via .NET, bir küre ağını Draco dosyasına doğrudan bir sahne oluşturmadan [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) sınıfı yöntemini kullanarak kodlamanıza izin verir. Aşağıdaki kod parçacığı, bu işlevselliğin nasıl kullanılacağını gösterir:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")

{{< /highlight >}}
#  **Encode loud phere as loud ointloud loud**
Aspose.3D for Python via .NET allows encoding a sphere mesh to Draco file as a point cloud using the [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) method of [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoSaveOptions

options = DracoSaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc", options)

{{< /highlight >}}
#  **Örgüyü PLY olarak kodlayın**
Aspose.3D for Python via .NET allows encoding a mesh to PLY file directly without building a scene using the [Encode](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [PlyFormat ](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)class. The following code snippet shows how to use this functionality:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Ağını PLY 'dan çöz**
Aspose.3D for Python via .NET, [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) sınıfı yöntemini kullanarak bir örgü/nokta bulutunun bir PLY dosyasından kodlanmasını sağlar. Aşağıdaki kod parçacığı, bu işlevselliğin nasıl kullanılacağını gösterir:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Export to PLY as PointCloud**
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
#  **Export 3D Scene as Point Cloud**
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

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
