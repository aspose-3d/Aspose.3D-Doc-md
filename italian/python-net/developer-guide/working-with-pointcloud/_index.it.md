---
title: Lavorare con PointCloud
type: docs
weight: 150
url: /it/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET consente di decodificare una mesh da un file Draco direttamente senza creare una scena utilizzando il metodo Decode della classe DracoFormat.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.7 o maggiore.

{{% /alert %}} 
#  **Decodificare la maglia**
Aspose.3D for Python via .NET consente di decodificare direttamente una mesh da un file Draco senza creare una scena utilizzando il metodo [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))

{{< /highlight >}}
#  **Code Mesh**
Aspose.3D for Python via .NET consente di codificare direttamente una mesh a sfera in un file Draco senza creare una scena utilizzando il metodo [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")

{{< /highlight >}}
#  **Codificare sfera come PointCloud**
Aspose.3D for Python via .NET consente di codificare una mesh sfera in file Draco come nuvola di punti utilizzando il metodo [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoSaveOptions

options = DracoSaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc", options)

{{< /highlight >}}
#  **Codificare la maglia fino a PLY**
Aspose.3D for Python via .NET consente di codificare direttamente un file mesh in PLY senza creare una scena utilizzando il metodo [Codifica](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) della classe [Formato ply](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Decodificare mesh a partire da PLY**
Aspose.3D for Python via .NET consente di decodificare una nuvola mesh/point da un file PLY utilizzando il metodo [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Esporta a PLY come PointCloud**
Aspose.3D for Python via .NET consente di esportare una scena a PLY come PointCloud utilizzando il metodo [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import PlySaveOptions

options = PlySaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply", options)

{{< /highlight >}}
#  **Esporta 3D scena come Point Cloud**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 

Aspose.3D for Python via .NET consente di esportare una scena 3D come PointCloud utilizzando la proprietà [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) della classe [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Il seguente frammento di codice mostra come utilizzare questa funzionalità:

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
