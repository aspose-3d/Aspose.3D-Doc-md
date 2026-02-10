---
title: Работа с PointCloud
type: docs
weight: 150
url: /ru/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET позволяет декодировать сетку из Draco файла напрямую без построения сцены с использованием метода Decode класса DracoFormat.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,7 или выше.

{{% /alert %}} 
#  **Декодирование сетки**
Aspose.3D for Python via .NET позволяет декодировать сетку из Draco файла напрямую без построения сцены с использованием метода [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))

{{< /highlight >}}
#  **Кодировать сетку**
Aspose.3D for Python via .NET позволяет напрямую кодировать сетку сферы в Draco файл без построения сцены методом [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")

{{< /highlight >}}
#  **Кодировать сферу как PointCloud**
Aspose.3D for Python via .NET позволяет кодировать сферическую сетку в Draco файл как облако точек, используя метод [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoSaveOptions

options = DracoSaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc", options)

{{< /highlight >}}
#  **Кодировать сетку в PLY**
Aspose.3D for Python via .NET позволяет кодировать сетку в PLY файл напрямую без построения сцены с использованием метода [Код](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [Формат PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Декодирование сетки от PLY**
Aspose.3D for Python via .NET позволяет декодировать облако ячеек/точек из файла PLY методом [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Экспортировать в PLY как PointCloud**
Aspose.3D for Python via .NET позволяет экспортировать сцену в PLY как PointCloud, используя метод [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import PlySaveOptions

options = PlySaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply", options)

{{< /highlight >}}
#  **Экспортировать сцену 3D как облако точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for Python via .NET позволяет экспортировать сцену 3D как PointCloud, используя свойство [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) класса [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

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
