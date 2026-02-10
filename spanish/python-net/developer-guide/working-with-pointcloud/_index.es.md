---
title: Trabajar con PointCloud
type: docs
weight: 150
url: /es/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET permite decodificar una malla desde un archivo Draco directamente sin construir una escena usando el método Decode de la clase DracoFormat.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,7 o superior.

{{% /alert %}} 
#  **Decodificar malla**
Aspose.3D for Python via .NET permite decodificar una malla de un archivo Draco directamente sin construir una escena usando el método [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))

{{< /highlight >}}
#  **Codificar malla**
Aspose.3D for Python via .NET permite codificar una malla de esfera en un archivo Draco directamente sin construir una escena usando el método [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")

{{< /highlight >}}
#  **Codificar Esfera como PointCloud**
Aspose.3D for Python via .NET permite codificar una malla de esfera en un archivo Draco como una nube de puntos utilizando el método [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoSaveOptions

options = DracoSaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc", options)

{{< /highlight >}}
#  **Encode Mesh a PLY**
Aspose.3D for Python via .NET permite codificar una malla en un archivo PLY directamente sin construir una escena usando el método [Codificar](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la clase [PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Decodificar malla desde PLY**
Aspose.3D for Python via .NET permite decodificar una malla/nube de puntos a partir de un archivo PLY utilizando el método [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Exportar a PLY como PointCloud**
Aspose.3D for Python via .NET permite exportar una escena a PLY como PointCloud utilizando el método [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import PlySaveOptions

options = PlySaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply", options)

{{< /highlight >}}
#  **Exportar escena 3D como nube de puntos**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 

Aspose.3D for Python via .NET permite exportar una escena 3D como PointCloud usando la propiedad [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) de la clase [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:

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
